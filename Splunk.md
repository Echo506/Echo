
# 📋 **Note:**

My purpose is to investigate this tool further and make the most of it for enterprise protection. These notes are not intended to be a complete explanation of the course; they are notes that I consider important in case they are needed. To understand all the information, you can check the official page where the complete course is located. Of course, if you have any questions or queries and I can help you, send me a message, and I will gladly assist you in any way I can.

---

# **🔗 References:**

I have taken as reference the material from the official Splunk page, which offers free and paid courses:

* [Splunk Training & Certification Overview](https://www.splunk.com/en_us/training/free-courses/overview.html)

---

# **Introduction to Splunk**

## **What is Splunk?**

Splunk is a **data analytics platform** primarily used for **monitoring, searching, and analyzing machine-generated data**.

### **Splunk Enterprise**

Splunk Enterprise offers key functionalities including:

* **Index**: For data ingestion and storage.
* **Search & Reporting**: For querying and generating insights.
* **Using Search**: The core way to interact with data.

**Commands that create statistics and visualizations are called transforming commands.**

### **Exploring Events**

* Events often contain keywords like `failed`.

### **Using Search Terms**

* Wildcards like `fail*` can be used to broaden searches.
* **Boolean operations** have a specific **order of evaluation**:
    1.  `NOT`
    2.  `OR`
    3.  `AND`

### **What are Commands?**

Splunk searches are built using a combination of:

* **Search Terms**
* **Commands**
* **Functions**
* **Arguments**
* **Clauses**

**Example Search String:**

```splunk
index=network sourcetype=cisco_wsa_squid usage=Violation
| stats count(usage) as Visits by cs_username
| search Visits > 1
````

Common default fields include: `index`, `source`, `host`, `sourcetype`.

-----

### **What are Knowledge Objects?**

Knowledge objects are configurations that enrich and make sense of your data in Splunk.

#### **Data Interpretation**

These help Splunk understand and extract meaningful information from raw events.

  * **Fields**: Automatically extracted or user-defined data points (e.g., `action`, `categoryID`, `clientip`, `product_name`).
  * **Field Extractions**: Rules to define and extract custom fields.
  * **Calculated Fields**: Fields derived from existing fields using expressions.

#### **Data Classification**

These categorize events for easier analysis and reporting.

  * **Event Types**: Classify events based on search criteria.
  * **Transactions**: Group related events into single logical transactions.

#### **Data Normalization**

These standardize data for consistent searching.

  * **Tags**: Assign keywords to field values or event types.
  * **Field Aliases**: Create alternative names for existing fields.

#### **Data Models**

  * **Hierarchically structured Datasets**: Provide a standardized way to navigate data for specific use cases.

#### **Data Enrichment**

These add external context or additional information to your events.

  * **Lookups**: Enrich events with data from external files (e.g., CSV).
  * **Workflows**: Define actions to take on search results (e.g., launching an external URL).

#### **Creating Reports**

Reports are saved searches that can be displayed in various formats.

##### **Command Example 1:**

```splunk
index=security sourcetype=linux_secure host!=mail* "Failed password" src_ip=*
| iplocation src_ip
| top limit=20 Country
```

**Explanation of the command:**

  * `index=security`: This specifies the Splunk index to search in. In this case, it's looking in the `security` index.
  * `sourcetype=linux_secure`: Filters the results to only include events with the `linux_secure` sourcetype, which typically logs authentication events from Linux systems (like SSH login attempts).
  * `host!=mail*`: Excludes any hosts that start with "mail". For example, `mail01`, `mailserver` will be excluded from the results.
  * `"Failed password"`: Searches for log entries that contain the exact phrase "Failed password", indicating failed login attempts.
  * `src_ip=*`: Ensures that only events with a source IP address (`src_ip`) are included.
  * `| iplocation src_ip`: This is a pipeline command (`|`) that takes the previous search results and enriches them using the `iplocation` command. It uses the `src_ip` field to add geographic information such as `Country`, `City`, `Region`, etc.
  * `| top limit=20 Country`: This command counts the most frequent values of the `Country` field and returns the **top 20 countries** based on the number of failed login attempts. It’s sorted by count in descending order.

##### **Command Example 2:**

```splunk
index=security sourcetype=linux_secure host!=mail* "Failed password" src_ip=*
| iplocation src_ip
| geostats count by Country
```

**Explanation of the `geostats` command:**

  * `| geostats count by Country`: This command aggregates the number of events (`count`) grouped by `Country`, and prepares the data for use in geographical visualizations, such as map charts.
  * `geostats` is like `stats`, but it is **optimized for geographic visualizations**. It also automatically adds latitude and longitude fields for plotting countries on a map.

### **Creating Dashboards**

Dashboards are interactive displays of reports and visualizations.

  * **Visualization**: Select the type of chart or table.
  * **New Dashboard**: Start a new dashboard.
  * **Report**: Convert a saved search into a report.
  * **Add panel**: Add reports or visualizations as panels to a dashboard.

### **Dashboard Studio**

Splunk's Dashboard Studio provides enhanced layout options:

  * **Absolute**: For precise pixel-perfect positioning.
  * **Grid**: For responsive, column-based layouts.

### **Additional Resources**

  * [Splunk Training & Education](https://www.splunk.com/en_us/training.html)
  * [Splunk Documentation](https://docs.splunk.com/)
  * [Splunk Lantern](https://lantern.splunk.com/)

<!-- end list -->

```
```
