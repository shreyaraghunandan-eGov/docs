# DIGIT 2.0 \(30.07.2020\)

### **Release Summary:** <a id="Release-DIGIT2.0(30.07.2020)-ReleaseSummary:"></a>

* DIGIT 2.0 is a baselined release that has got very few functional changes, but more of a non-functional standardization changes.
* Functional: Introducing advance payment feature and Advance collection integration with W/S.
* Non-functional: Upgrading spring boot and tracer version of all the backend services to enhance the range of non-functional benefits like performance, metrics, and security. Also all digit services/configs are baselined to follow the Semantic Versioning. These would enable the partner eco-system, system Integrators and state teams for an easy on-going upgrades and integrations.

### Upgrade Instructions: <a id="Release-DIGIT2.0(30.07.2020)-UpgradeInstructions:"></a>

* DIGIT 2.0 is a baselined release - considering simplification and standardization as a theme. It is strongly recommended all state teams upgrade to leverage benefits.
  * All services versioning will follow [**SemVer 2.0**](https://medium.com/@pmuens/understanding-semver-3f75d11b4d)**,** naming conventions and Git Tagging are improved for better tracing.
  * Next release we might have few more enhancements to the services naming conventions and handling MDMS and Configs better.
* **Impact**: Functionally, the upgrade to DIGIT 2.0 should not impact the existing environments.

### What has been changed: <a id="Release-DIGIT2.0(30.07.2020)-Whathasbeenchanged:"></a>

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p><b>New Features:</b>
        </p>
        <ul>
          <li>Ability to handle <a href="https://digit-discuss.atlassian.net/wiki/spaces/ED/pages/604307457/Release+Notes+for+Advance+Payment+implementation+in+W+S">advanced payments</a> -
            platform and Reference implementation in W&amp;S.</li>
          <li>Advance Collection integration with W&amp;S
            <ul>
              <li>API Contracts</li>
            </ul>
          </li>
        </ul>
        <p><b>Enhancements:</b>
        </p>
        <ul>
          <li>Bulk persister changes to support bulk persisting for migration in Persister
            Service.</li>
          <li>Localization URL params to be changed to request params in Localization
            service</li>
          <li>Receipt download link in SMS and email notifications.</li>
          <li>Rainwater Harvesting attribute in Property Service</li>
          <li>Filestore service enhancement - Support for SDC and S3 implementation.</li>
          <li>Maven dependencies upgrade and merging the backend services to the master
            branch (Upgraded Tracer to 2.0.0, spring boot to 2.2.6, flyway-core to
            6.4.3, etc along with code cleanup) for all the services across the services.
            The Changelog has been added.</li>
          <li>Baseline versioning of all the services as per the streaming strategy.</li>
          <li>UI Enhancements
            <ul>
              <li>Generalized Client-side PDF generation component and integration with
                Property, Fire NOC, Trade License, and W&amp;S applications).</li>
              <li>Generalize acknowledgment screens component</li>
              <li>MDMS namespace common component and integration with PT and TL modules.</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left">
        <p><b>New Features:</b>
        </p>
        <p><b>Infra/Ops Simplification &amp; Enablement:</b>
        </p>
        <ul>
          <li>Infra &amp; Service monitoring v1.0.0 (Prometheus, Alertmanager &amp;
            Grafana)
            <ul>
              <li>Cluster Resource monitoring</li>
              <li>Request Traffic monitoring</li>
              <li>DIGIT Service monitoring</li>
            </ul>
          </li>
          <li>All Java based services SpringBoot upgraded from 1.5.X to 2.2.6 for better
            security, performance and metrics.</li>
          <li>Backbone Services migrated to Helm templates to ease deployment on kubernetes.</li>
          <li>Introduced Minio as a digit platform service for SDCs to leverage S3 like
            object storage feature.</li>
          <li>DIGIT on Spot Instances for AWS users, saves 60% of the cloud cost.</li>
          <li>Configurable SSO with GitHub or Google SSO oauth for all the Infra apps
            like Jaeger, Grafana, Kibana.</li>
          <li>DIGIT Jenkins as a service</li>
          <li>DIGIT CI/CD <a href="https://github.com/egovernments/CIOps">Pipelines-as-a-service</a>
          </li>
        </ul>
        <p><b>Enhancements:</b>
        </p>
        <ul>
          <li>Versioned Git Tags for all the services</li>
          <li>Versioned MDMS and Config data.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Services and build artefact Details: <a id="Release-DIGIT2.0(30.07.2020)-ServicesandbuildartefactDetails:"></a>

<table>
  <thead>
    <tr>
      <th style="text-align:left">Category</th>
      <th style="text-align:left">Services</th>
      <th style="text-align:left">GIT TAGS</th>
      <th style="text-align:left">Docker Artifact ID</th>
      <th style="text-align:left">MDMS Changes</th>
      <th style="text-align:left">Config Changes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>Frontend</b>  <a href="https://github.com/egovernments/municipal-services/tree/v2.0"><b>v2.0</b></a>
      </td>
      <td style="text-align:left">Citizen</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/frontend/tree/citizen-v1.0.0">citizen-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>citizen:v1.0.0-5c70cea1d</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Employee</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/frontend/tree/employee-v1.0.0">employee-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>employee:v1.0.0-5c70cea1d</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">DSS Dashboard</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/frontend/tree/dashboard-v1.0.0">dashboard-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>dss-dashboard:v1.0.0-766ef5a0a</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Core Services</b>  <a href="https://github.com/egovernments/core-services/tree/v2.0"><b>v2.0</b></a>
      </td>
      <td style="text-align:left">Encryption</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/enc-service-v1.1.0">enc-service-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-enc-service:v1.1.0-f9375a4</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Searcher</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/searcher-v1.1.0">searcher-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-searcher:v1.1.0-59d3598</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Payment Gateway</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/pg-service-v1.1.0">pg-service-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-pg-service:v1.1.0-f9375a4</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Filestore</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/filestore-v1.2.0">filestore-v1.2.0</a>
      </td>
      <td style="text-align:left"><code>egov-filestore:v1.2.0-3acc52b</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Zuul - API Gateway</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/zuul-v1.1.0">zuul-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>zuul:v1.1.0-582ddd0</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Mail Notification</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/notification-mail-v1.1.0">notification-mail-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-notification-mail:v1.1.0-40b5f2d</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">SMS Notification</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/notification-sms-v1.1.0">notification-sms-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-notification-sms:v1.1.0-245443e</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Localization</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/localization-v1.1.0">localization-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-localization:v1.1.0-f9375a4</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1073">PR-1073</a>
          </li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://raw.githubusercontent.com/egovernments/releasekit/master/localisation/data.json">Localisation data</a>
          </li>
          <li><a href="https://raw.githubusercontent.com/egovernments/releasekit/master/localisation/ws_30_07_2020.json"><b>WS Localisation data</b></a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Persister</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/persister-v1.1.0">persister-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-persister:v1.1.0-9994513</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">ID Gen</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/idgen-v1.2.0">idgen-v1.2.0</a>
      </td>
      <td style="text-align:left"><code>egov-idgen:v1.2.0-f9375a4</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">User</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/user-v1.2.1">user-v1.2.1</a>
      </td>
      <td style="text-align:left"><code>egov-user:v1.2.1-4976757</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">User Chatbot</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/user-chatbot-v1.2.1">user-chatbot-v1.2.1</a>
      </td>
      <td style="text-align:left"><code>egov-user-chatbot:v1.2.1-4976757</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">MDMS</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/mdms-service-v1.3.0">mdms-service-v1.3.0</a>
      </td>
      <td style="text-align:left"><code>egov-mdms-service:v1.3.0-e50b9eb</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">URL Shortening</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/url-shortening-v1.0.0">url-shortening-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>egov-url-shortening:v1.0.0-40cc090</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Indexer</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/indexer-v1.1.0">indexer-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-indexer:v1.1.0-07592ae</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/configs/commit/47528052b4904ce5ab679324f13165458a83d05a">egov-bpa-indexer.yml</a>
          </li>
          <li><a href="https://github.com/egovernments/configs/commit/47528052b4904ce5ab679324f13165458a83d05a">rainmaker-bpastakeholder-indexer.yml</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Report</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/report-v1.3.0">report-v1.3.0</a>
      </td>
      <td style="text-align:left"><code>report:v1.3.0-28b3c97</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1170">PR-1170</a>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Workflow</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/workflow-v2-v1.1.0">workflow-v2-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-workflow-v2:v1.1.0-42786ef</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">PDF Generator</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/pdf-service-v1.1.0">pdf-service-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>pdf-service:v1.1.0-09b11d9</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Chatbot</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/chatbot-v1.0.0">chatbot-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>chatbot:v1.0.0-f905f54</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Access Control</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/accesscontrol-v1.1.0">accesscontrol-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-accesscontrol:v1.1.0-f9375a4</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Location</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/location-v1.1.0">location-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-location:v1.1.0-f9375a4</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">OTP</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/otp-v1.2.0">otp-v1.2.0</a>
      </td>
      <td style="text-align:left"><code>egov-otp:v1.2.0-f9375a4</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">User OTP</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/core-services/tree/user-otp-v1.1.0">user-otp-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>user-otp:v1.1.0-2f36d3a</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Business Services</b>  <a href="https://github.com/egovernments/business-services/tree/v2.0"><b>v2.0</b></a>
      </td>
      <td style="text-align:left">Apportion</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/business-services/tree/apportion-service-v1.1.0">apportion-service-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-apportion-service:v1.1.0-5553009</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Collection</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/business-services/tree/collection-services-v1.1.0">collection-services-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>collection-services:v1.1.0-afb3913</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1106">PR-1106</a>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Billing</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/business-services/tree/billing-service-v1.1.0">billing-service-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>billing-service:v1.1.0-4367159</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/configs/commit/0f3708cdcf6fba00aa36aab5baeae9a7eeb3ab62#diff-9352898a62515ccb3822f24506a37090">bill-genie.yml</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">HRMS</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/business-services/tree/hrms-v1.1.0">hrms-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-hrms:v1.1.0-43cb793</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Dashboard Analytics</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/business-services/tree/dashboard-analytics-v1.1.0">dashboard-analytics-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>dashboard-analytics:v1.1.0-de5ab6d</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Dashboard Ingest</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/business-services/tree/dashboard-ingest-v1.1.0">dashboard-ingest-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>dashboard-ingest:v1.1.0-5cc43bf</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">EGF Instrument</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/business-services/tree/egf-instrument-v1.1.0">egf-instrument-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egf-instrument:v1.1.0-87dfb2d</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">EGF Master</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/business-services/tree/egf-master-v1.1.0">egf-master-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egf-master:v1.1.0-9959f29</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Finance Collection Voucher Consumer</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/business-services/tree/finance-collections-voucher-consumer-v1.1.0">finance-collections-voucher-consumer-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>finance-collections-voucher-consumer:v1.1.0-004e14a</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Municipal Services</b>  <a href="https://github.com/egovernments/municipal-services/releases/tag/v2.0"><b>v2.0</b></a>
      </td>
      <td style="text-align:left">Trade License</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/tl-services-v1.1.0">tl-services-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>tl-services:v1.1.0-be11a0f5</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1160">PR-1160</a>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Trade License Calculator</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/tl-calculator-v1.1.0">tl-calculator-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>tl-calculator:v1.1.0-c52ffe21</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1125">PR-1125</a>
          </li>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1133">PR-1133</a>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Fire NOC</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/firenoc-services-v1.0.0">firenoc-services-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>firenoc-services:v1.0.0-4abf83d8</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Fire NOC Calculator</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/firenoc-calculator-v1.0.0">firenoc-calculator-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>firenoc-calculator:v1.0.0-ae96e930</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Property Services</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/property-services-v1.0.0">property-services-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>property-services:v1.0.0-ecf3410a</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Property Tax Calculator</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/pt-calculator-v2-v1.1.0">pt-calculator-v2-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>pt-calculator-v2:v1.1.0-63e20365</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Property Tax</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/pt-services-v2-v1.0.0">pt-services-v2-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>pt-services-v2:v1.0.0-ecf3410a</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Water Charges</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/ws-services-v1.0.0">ws-services-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>ws-services:v1.0.0-67c2139c</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1043">PR-1043</a>
          </li>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1058">PR-1058</a>
          </li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/configs/pull/357">PR-357</a>
          </li>
          <li><a href="https://github.com/egovernments/configs/pull/340">PR-340</a>
          </li>
          <li><a href="https://github.com/egovernments/configs/commit/900e8e1c59ebc12f4bea49f52063f524aabf3830#diff-b5d08abcd9524da252a33fcff4c515f8">ws-bill.json</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Water Charges Calculator</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/ws-calculator-v1.0.0">ws-calculator-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>ws-calculator:v1.0.0-d7529cf4</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/configs/pull/342">PR-342</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Sewerage Charges</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/sw-services-v1.0.0">sw-services-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>sw-services:v1.0.0-a2ee0ed4</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/configs/commit/d213b8fbc71c8adc67df393b30c8be9ea923e24f#diff-cad1acac07cf6e6c1843536937285a4d">water-meter.yml</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Sewerage Charges Calculator</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/sw-calculator-v1.0.0">sw-calculator-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>sw-calculator:v1.0.0-67e5a1bc</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">BPA Calculator</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/bpa-calculator-v1.0.0">bpa-calculator-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>bpa-calculator:v1.0.0-1aeb87df</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/996/files">PR-996</a>
          </li>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/995/files">PR-995</a>
          </li>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1162/files">PR-1162</a>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">BPA Services</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/bpa-services-v1.0.0">bpa-services-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>bpa-services:v1.0.0-b5520589</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1118/files">PR-1118</a>
          </li>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1062/files">PR-1062</a>
          </li>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1019/files">PR-1019</a>
          </li>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1016/files">PR-1016</a>
          </li>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1008/files">PR-1008</a>
          </li>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1007/files">PR-1007</a>
          </li>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/1006">PR-1006</a>
          </li>
          <li><a href="https://github.com/egovernments/egov-mdms-data/pull/997">PR-997</a>
          </li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li><a href="https://github.com/egovernments/configs/commit/5682f1adb60b40663fe13d545e0c865ad4537b08">land-persister.yml</a>
          </li>
          <li><a href="https://github.com/egovernments/configs/commit/9ae764474a702249cd3aaefa806a3331a37e0364">bpa-persister.yml</a>
          </li>
          <li><a href="https://github.com/egovernments/configs/commit/47528052b4904ce5ab679324f13165458a83d05a">bpa-revocation.json</a>
          </li>
          <li><a href="https://github.com/egovernments/configs/commit/47528052b4904ce5ab679324f13165458a83d05a">buildingpermit-low.json</a>
          </li>
          <li><a href="https://github.com/egovernments/configs/commit/47528052b4904ce5ab679324f13165458a83d05a">buildingpermit.json</a>
          </li>
          <li><a href="https://github.com/egovernments/configs/commit/47528052b4904ce5ab679324f13165458a83d05a">occupancy-certificate.json</a>
          </li>
          <li><a href="https://github.com/egovernments/configs/commit/5f7eafdf3339d49a736d31c50037333a11c0f114">noc-persister.yml</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">User Event</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/user-event-v1.1.0">user-event-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-user-event:v1.1.0-e518861c</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">PGR</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/rainmaker-pgr-v1.1.0">rainmaker-pgr-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>rainmaker-pgr:v1.1.0-5058d47e</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Land Services</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/municipal-services/tree/land-services-v1.0.0">land-services-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>land-services:v1.0.0-ae5cee9f</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Utilities Services</b>  <a href="https://github.com/egovernments/utilities/tree/v2.0"><b>v2.0</b></a>
      </td>
      <td style="text-align:left">Custom Consumer</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/utilities/tree/custom-consumer-v1.1.0">custom-consumer-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-custom-consumer:v1.1.0-7a6db73</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">PDF</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/utilities/tree/pdf-v1.1.0">pdf-v1.1.0</a>
      </td>
      <td style="text-align:left"><code>egov-pdf:v1.0.0-009661c</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Others Service</b>  <a href="https://github.com/egovernments/eGov-dcr-service/releases/tag/v2.0"><b>v2.0</b></a>
      </td>
      <td style="text-align:left">eDCR</td>
      <td style="text-align:left"><a href="https://github.com/egovernments/eGov-dcr-service/tree/egov-edcr-v1.0.0">egov-edcr-v1.0.0</a>
      </td>
      <td style="text-align:left"><code>egov-edcr:v1.0.0-04ff1e5</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Finance</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>InfraOps v2.0</b>
      </td>
      <td style="text-align:left">Prometheus</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"><a href="http://quay.io/prometheus/prometheus:v2.15.2">quay.io/prometheus/prometheus:v2.15.2</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Prometheus Operator</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"><a href="http://quay.io/coreos/prometheus-operator:v0.37.0">quay.io/coreos/prometheus-operator:v0.37.0</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Kubestate metrics</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"><a href="http://quay.io/coreos/kube-state-metrics:v1.9.7">quay.io/coreos/kube-state-metrics:v1.9.7</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Kuberhealthy</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Grafana</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">grafana/grafana:7.0.5</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Alert manager</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"><a href="http://quay.io/prometheus/alertmanager:v0.20.0">quay.io/prometheus/alertmanager:v0.20.0</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Minio</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">PG Admin</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Spot Instance Terminator</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">kubeaws/kube-spot-termination-notice-handler:1.13.7-1</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">OAuth for Kibana, Jaeger</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Digit-Jenkins-as-service</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">DIGIT-CI/CD-as-service</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Deprecated</b>
      </td>
      <td style="text-align:left">egov-data-uploader</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">egov-common-masters</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">egov-index-custom-consumer</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### **DIGIT 2.0 - Technical/Configuration documents created/updated** <a id="Release-DIGIT2.0(30.07.2020)-DIGIT2.0-Technical/Configurationdocumentscreated/updated"></a>

* **Backend Services**
  * [Advance Payment](https://digit-discuss.atlassian.net/l/c/1P512Vzx)
  * [Kafka Connect for reindex](https://digit-discuss.atlassian.net/l/c/41XVUCh6)
  * [TL Service Renewal Upgradation](https://digit-discuss.atlassian.net/l/c/cRAR1xcf)
  * [Filestore service](https://digit-discuss.atlassian.net/wiki/spaces/EPE/pages/37060620/File-Store-Service?atlOrigin=eyJpIjoiOWQwYWZmYjNkNTU0NDFlMzk4YjdiNTk1YTI3ZDY3NTciLCJwIjoiYyJ9)
  * [Persister Service](https://digit-discuss.atlassian.net/l/c/hydmp2YA)
  * [Collection Migration v1 to v2](https://digit-discuss.atlassian.net/wiki/spaces/EPE/pages/152567827/Collection+Migration+V1+to+V2?atlOrigin=eyJpIjoiNjEwNjQ1MWE5ZDNmNGU5Nzk0MWI5YWJlNjU0N2E1YWQiLCJwIjoiYyJ9)
  * [Consumer Code Uniqueness Migration](https://digit-discuss.atlassian.net/wiki/spaces/EPE/pages/155910170/Consumer+Code+Uniqueness+Migration?atlOrigin=eyJpIjoiMTc5Y2Q1OWQ0NDBmNDA2MmJhNjRjZGY5NjY3ZTJjYWQiLCJwIjoiYyJ9)
  * [Property Registry Migration](https://digit-discuss.atlassian.net/l/c/dgM6oHg1)
  * [Notification SMS service](https://digit-discuss.atlassian.net/l/c/0y774J0V)
  * [Water Service](https://digit-discuss.atlassian.net/wiki/spaces/EPE/pages/328925216/Water+Service+-+Technical+Document?atlOrigin=eyJpIjoiNDM4Yjc3MmJmNDBiNDViZGEwZjJmYTg2MzVhNDdkOTgiLCJwIjoiYyJ9)
  * [Sewerage Service](https://digit-discuss.atlassian.net/l/c/PM2Ho3A1)
  * [Water Calculator Service](https://digit-discuss.atlassian.net/l/c/p3MGjvPw)
  * [Sewerage Calculator Service](https://digit-discuss.atlassian.net/l/c/o0gRiR1n)
  * [W&S Promotion document](https://digit-discuss.atlassian.net/l/c/Z2yYBY2b)
* **UI Technical documentations**
  * [PGR](https://digit-discuss.atlassian.net/l/c/U01pjZQ1)
  * [Property Tax](https://digit-discuss.atlassian.net/wiki/spaces/EGR/pages/53542929/Property+Tax+-+UI?atlOrigin=eyJpIjoiNzkwMGY4ZWYyYjJhNDVhOWEzMTg4ZWExNTg0MGU0YjgiLCJwIjoiYyJ9)
  * [Trade License](https://digit-discuss.atlassian.net/l/c/57TggeCL)
  * [Fire NOC](https://digit-discuss.atlassian.net/l/c/fcwPm0NC)
  * [Bill Genie](https://digit-discuss.atlassian.net/wiki/spaces/EGR/pages/436502610/BillGenie?atlOrigin=eyJpIjoiN2EzZmY2ZjFlYzIxNDc2Zjk4YzIwM2FmOGI1NmM1MDAiLCJwIjoiYyJ9)
  * [MCS](https://digit-discuss.atlassian.net/wiki/spaces/EGR/pages/438894719/Universal+Collection?atlOrigin=eyJpIjoiNjAzNzBiMTAwMzNlNDk2NDk0ZTQxNjdlMzMwYzE5N2IiLCJwIjoiYyJ9)
  * [Common Pay](https://digit-discuss.atlassian.net/l/c/NjoYpKzK)
  * [Advance Payment](https://digit-discuss.atlassian.net/l/c/i7T9cbxf)
  * [mSeva 2.0](https://digit-discuss.atlassian.net/l/c/QX3zRcjW)
  * [Water & Sewerage](https://digit-discuss.atlassian.net/l/c/Eg1iS0ba)
  * [MDMS UI Configurations](https://digit-discuss.atlassian.net/l/c/AfRS5iZw)
  * [Required documents dialog implementation](https://digit-discuss.atlassian.net/wiki/spaces/EGR/pages/449085476/Required+documents+dialog+implementation?atlOrigin=eyJpIjoiNDEwZDdkNWYzY2EwNDRkZWE0Nzg2NTcwOTM5NDg1YzMiLCJwIjoiYyJ9)
  * [Generation of Acknowledgement PDF](https://digit-discuss.atlassian.net/l/c/dVxJH2B5)
  * [How to add dynamic dropdown for MDMS data ](https://digit-discuss.atlassian.net/wiki/spaces/EGR/pages/450789466/How+to+add+dynamic+drop+down+for+mdms+data?atlOrigin=eyJpIjoiNDY0ZGQxY2RhNTBkNDExOWE4ZTc1MTUxOTk4MTZmOTAiLCJwIjoiYyJ9)
  * [Common Acknowledgment screens](https://digit-discuss.atlassian.net/wiki/spaces/EGR/pages/572522501/Acknowledgment+screens?atlOrigin=eyJpIjoiNWI5YzdmZDkyNThmNGI4MGFlMjI2MDg0NzRkMWQ4ZTgiLCJwIjoiYyJ9)
* **Infra/deployment**
  * [Monitoring & Alerting](https://github.com/egovernments/eGov-infraOps/commit/274aab0e90a10673972ddc769f2fc89015f0fe8d)
  * [SSO OAuth \(GitHub\)](https://github.com/egovernments/eGov-infraOps/commit/4aae58e8560c726a44c9347795fd9db80aaed6c8) for Kibana, Jaeger, etc
  *  [Grafana](https://github.com/egovernments/eGov-infraOps/commit/c7a4c3d5eb8b188e5083f3e0f33a9405bb995895) dashboard for Infra and Service monitoring
  * [Jenkins as a service](https://github.com/egovernments/eGov-infraOps/commit/274aab0e90a10673972ddc769f2fc89015f0fe8d) for CI/CD
  * Minio [Helm templates](https://github.com/egovernments/eGov-infraOps/pull/764/files)

