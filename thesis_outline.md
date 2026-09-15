# Diploma Thesis Outline

## Title

**ArtAdmin – Provenance Management, Image-Based Object Identification and Depth-Camera-Assisted Measurement for Historical Objects**

## Preliminary pages

- Title page
- Declaration of Academic Honesty
- Abstract
- Zusammenfassung / German version of Abstract
- Table of Contents
- List of Figures
- List of Tables
- List of Abbreviations
- List of Terms, optional


## 1. Introduction

Expected length: 5–7 pages

### 1.1 Project context [W,H]

- Introduction to the cooperation with St. Florian Monastery.
- Relevance of historical objects and collection documentation.
- Role of ArtAdmin as a diploma-thesis project.
- Joint project scope and division of responsibilities.

### 1.2 Initial situation [W,H]

- Existing use of spreadsheets, analogue documents and heterogeneous records.
- Fragmented information about objects, provenance, sources, images and measurements.
- Practical difficulties when searching for objects or comparing records.
- Need for a central, structured and maintainable information system.

### 1.3 Problem statement [W,H]

The chapter should formulate the problem as research and engineering questions:

- Which information must be recorded for historical objects and their provenance?
- Which data standards are suitable for structured and interoperable provenance documentation?
- To what extent can a depth camera support non-contact measurement of historical objects?
- How can image similarity search assist object identification and duplicate detection?
- How can these functions be integrated into a usable and traceable web application?

### 1.4 Objectives [W,H]

- Develop a web application for structured object and provenance management.
- Design a data model informed by established cultural-heritage and provenance standards.
- Integrate image-based similarity search and duplicate detection.
- Investigate the suitability of a depth camera for object measurement.
- Evaluate accuracy, data quality, usability and practical limitations.

### 1.5 Scope and limitations [W,H]

- ArtAdmin is not intended to replace a complete museum collection-management system.
- The system does not provide legally binding provenance verification or ownership assessment.
- The depth-camera component focuses on measurement and selected 3D data processing, not on professional digitization of every object.
- Full mesh reconstruction is not the primary objective.
- Camera expenditure is limited to approximately 500€.
- Results depend on the available test objects, reference measurements, lighting conditions and project time.

## 2. Current Situation

Expected length: 12–18 pages

### 2.1 Institutional and practical context [W]

- Characteristics of the collection and historical objects relevant to the project.
- Typical work performed by custodians, restorers, archive staff and administrators.
- Existing documents, spreadsheets, photographs and measurement records.
- Practical constraints when handling sensitive or valuable objects.

### 2.2 Current problems and requirements derived from practice [W]

- Unstructured or inconsistent terminology.
- Missing or uncertain values.
- Difficulties in finding related records.
- Lack of explicit source and time relationships.
- Limited change traceability.
- Risk of duplicate records.
- Manual effort required for measurements and comparisons.

### 2.3 Existing provenance and collection-data standards [H]

#### 2.3.1 W3C PROV

- Provenance concepts such as entities, activities and agents.
- Relevance to change history and traceability.
- Distinction between a general provenance model and a museum-specific object-data model.

#### 2.3.2 CIDOC Conceptual Reference Model 

- Event-oriented modelling of cultural-heritage information.
- Strengths for historical context, actors, places and events.
- Complexity and implementation implications.

#### 2.3.3 LIDO

- Role as an exchange format for museum and cultural-heritage object information.
- Relevance to object records and interoperability.

#### 2.3.4 Dublin Core and related metadata models

- General metadata concepts.
- Advantages for simple interoperability.
- Limitations for detailed provenance chains.

#### 2.3.5 SPECTRUM and Europeana Data Model

- Relevance to collection procedures and linked cultural-heritage data.
- Distinction between operational documentation, exchange formats and semantic models.

### 2.4 Existing solutions for collection management [W]

- Categories of existing museum and collection-management systems.
- Typical features: object records, media, loans, locations, conservation and search.
- Comparison with ArtAdmin’s limited project scope.
- Reasons why an existing system may not fully satisfy the specific requirements of St. Florian Monastery.

The final text should name only products that have been systematically investigated and should separate vendor documentation from peer-reviewed or official-standard evidence.

### 2.5 Existing approaches to object identification [W]

#### 2.5.1 Exact duplicate detection

- File hashes and their suitability for byte-identical files.
- Limitations when images are resized, recompressed or edited.

#### 2.5.2 Near-duplicate detection

- Perceptual hashes.
- Robustness and limitations under cropping, rotation and lighting changes.

#### 2.5.3 Local image features

- Feature points and descriptors.
- Suitability for partial matches and changed viewpoints.

#### 2.5.4 Deep image embeddings

- Feature extraction using pretrained or domain-adapted models.
- Similarity metrics such as cosine similarity.
- Need for threshold calibration and human verification.

### 2.6 Existing approaches to 3D measurement [H]

#### 2.6.1 Manual measurement

- Reference measuring tools and their practical advantages.
- Contact-related risks and operator dependency.

#### 2.6.2 Photogrammetry

- Image-based reconstruction and dependencies on texture, overlap, lighting and camera calibration.

#### 2.6.3 Depth cameras

- Stereo triangulation.
- Structured light.
- Time-of-flight measurement.
- Typical error sources for reflective, transparent, dark or thin structures.

#### 2.6.4 Existing camera classes and project constraints

- Consumer depth cameras.
- Professional scanners.
- Budget, SDK, range, portability and integration criteria.
- The RealSense D456 as the available project hardware.

## 3. Proposed Solution

Expected length: 15–22 pages

### 3.1 Solution overview [H]

- Purpose and target users of ArtAdmin.
- Main use cases.
- Scope of the first usable system version.
- Relationship between provenance management, object identification, image search and depth-camera measurement.

### 3.2 User roles and use cases [W]

- Custodian or collection staff.
- Restorer or conservation staff.
- Archive staff.
- Administrator.
- Authentication, authorization and role-specific capabilities.

Recommended use cases:

- Create and edit an object record.
- Record provenance events and sources.
- Upload and manage images and documents.
- Perform a measurement with the depth camera.
- Search using text, metadata and filters.
- Search for visually similar objects.
- Inspect the history of changes.

### 3.3 Requirements specification [W]

- Functional requirements with unique identifiers.
- Quality requirements.
- Prioritization into mandatory, desirable and optional requirements.
- Acceptance criteria.
- Traceability from requirements to implementation and test cases.

### 3.4 Decision methodology [H]

- Definition of evaluation criteria.
- Weighting and scoring method.
- Handling of qualitative and quantitative criteria.
- Limitations of decision matrices.
- Separation of evidence-based findings from project-specific preferences.

### 3.5 Decision on the provenance-data model [H]

- Comparison of W3C PROV, CIDOC CRM, LIDO, Dublin Core, SPECTRUM and a project-specific model.
- Selection of complementary rather than mutually exclusive concepts where appropriate.
- Justification of the model used by ArtAdmin.
- Mapping of object records, provenance events, agents, places, sources and media.
- Handling of uncertainty, missing values and conflicting historical evidence.

### 3.6 Decision on the depth-camera approach [H]

- Comparison of manual measurement, photogrammetry, depth-camera measurement and full 3D scanning.
- Evaluation criteria: cost, contactlessness, expected accuracy, data quality, processing effort, portability and integration.
- Decision to focus on measurement rather than complete mesh reconstruction, if supported by the performed experiments.
- Definition of the intended measurement output and its acceptable uncertainty.

### 3.7 Decision on image similarity and duplicate detection [W]

- Comparison of file hashes, perceptual hashes, local features and embeddings.
- Decision on a staged or combined approach.
- Definition of similarity categories.
- Human confirmation as part of the workflow.
- Risks of false positives and false negatives.

### 3.8 Decision on search and data storage [H]

- Relational database for structured data.
- Search index for full-text and filtered retrieval.
- Object storage for image and measurement files.
- Synchronization and consistency considerations.

### 3.9 Decision on architecture and deployment [H]

- Monolith versus service-oriented architecture.
- Local development, self-hosted deployment or cloud deployment.
- Docker and orchestration strategy.
- Authentication provider and authorization model.
- Backup, monitoring and maintenance considerations.

### 3.10 Proposed end-to-end workflow

#### 3.10.1 Object registration [H]

1. User authenticates.
2. User creates an object record.
3. Metadata, provenance information and sources are entered.
4. Images and documents are attached.
5. Optional depth-camera measurement is performed.
6. The record is validated and stored.
7. Search indexes and audit information are updated.

#### 3.10.2 Similarity search [W]

1. User uploads or selects an image.
2. The image is preprocessed.
3. Features or embeddings are generated.
4. Candidate records are retrieved.
5. Similarity scores and relevant metadata are displayed.
6. The user confirms, rejects or postpones the duplicate warning.

### 3.11 Security and integrity concept [H]

- Authentication and authorization.
- Role-based access control.
- Audit logging and version history.
- Integrity protection and its limitations.
- Precise use of terms such as *traceable*, *tamper-evident* and *tamper-resistant* instead of claiming absolute forgery protection.

## 4. Technical Description

Expected length: 35–50 pages

### 4.1 System architecture [H]

- Overall component architecture.
- Frontend, backend, databases, search engine, object storage, identity provider and camera component.
- Logical and deployment views.
- Main data flows.
- Synchronous and asynchronous communication.
- Error and recovery paths.

### 4.2 Frontend architecture and user interface [W]

- Angular application structure.
- Component and service responsibilities.
- Navigation and information architecture.
- Forms, validation and user feedback.
- Object list, filters and detail view.
- Provenance-entry interface.
- Media-management interface.
- Measurement interface.
- Similarity-search interface.
- Responsive design and accessibility measures.
- Design decisions for non-technical users.

### 4.3 Backend and API [H]

- ASP.NET Core architecture.
- Layering and separation of concerns.
- REST resources and endpoint groups.
- Request validation and error handling.
- OpenAPI documentation.
- Logging and health checks.
- Media handling.
- Search-index synchronization.
- API protection through authentication and authorization.

### 4.4 Object and provenance data model [H]

- Conceptual model.
- Entity-relationship model.
- Object, provenance event, agent, place, source, media and measurement entities.
- Relationship between object history and W3C PROV concepts.
- Mapping to CIDOC CRM and/or LIDO concepts where applicable.
- Controlled vocabularies and identifiers.
- Mandatory, optional and repeatable properties.
- Representation of uncertainty and unknown information.
- Versioning and audit records.

### 4.5 Data storage and media management [H]

- PostgreSQL schema and constraints.
- Indexes and query strategy.
- Storage of images, documents, depth frames and derived files.
- Metadata and content relationships.
- Backup and restore considerations.
- Data lifecycle and archival considerations.

### 4.6 Full-text search and filtering [H]

- Search-index structure.
- Document mapping and analyzers.
- Full-text queries.
- Filters, facets and sorting.
- Relevance and typo handling, if implemented.
- Indexing workflow and consistency behaviour.
- Search limitations and operational considerations.

### 4.7 Image similarity search [W]

#### 4.7.1 Processing pipeline

- Image upload.
- Validation and normalization.
- Optional resizing, cropping or background handling.
- Feature or embedding extraction.
- Storage and indexing of representations.
- Query-time retrieval.
- Ranking and result presentation.

#### 4.7.2 Similarity computation

- Cosine similarity and/or Euclidean distance.
- Normalization assumptions.
- Threshold selection.
- Candidate ranking.
- Difference between exact duplicates, near duplicates and semantically similar objects.

#### 4.7.3 Robustness considerations

- Perspective changes.
- Lighting and shadows.
- Background variation.
- Cropping and scale.
- Object ageing and surface changes.
- Similar-looking but distinct objects.

No claim should be made that image similarity alone proves object identity.

### 4.8 Depth camera and 3D measurement [H]

#### 4.8.1 Hardware and software setup

- RealSense D456 hardware.
- Connection and operating environment.
- Relevant librealsense functionality.
- Colour and depth streams.
- Camera calibration and alignment.

#### 4.8.2 Measurement principle

- Pixel coordinates and depth values.
- Transformation into camera-space coordinates.
- Selection of measurement points or regions.
- Calculation of length, width and height.
- Optional volume estimation and its assumptions.

#### 4.8.3 Preprocessing and data-quality handling

- Invalid depth values.
- Noise reduction.
- Outlier handling.
- Spatial filtering.
- Region selection and segmentation.
- Preservation of raw data for later verification.

#### 4.8.4 Measurement uncertainty

For every accuracy result, report:

- camera model and firmware or SDK version;
- measurement distance;
- viewing angle;
- object dimensions;
- material and surface properties;
- ambient and artificial lighting;
- measurement method;
- reference instrument and reference uncertainty;
- number of repetitions;
- mean error, absolute error and relative error;
- repeatability and observed outliers.

#### 4.8.5 Difference between measurement and 3D scanning

- Measurement aims to determine selected dimensions.
- A 3D scan aims to capture complete geometry, usually as a point cloud or mesh.
- Explain why the project focuses on reliable dimensions rather than promising complete geometric reconstruction.

#### 4.8.6 Limitations for historical objects

- Reflective or transparent surfaces.
- Very dark surfaces.
- Fine structures and thin edges.
- Occlusions and inaccessible areas.
- Small objects and minimum working distance.
- Object handling and conservation constraints.

### 4.9 Authentication, authorization and auditability [H]

- OAuth 2.0 and OpenID Connect roles in the system.
- Login and token flow.
- Role-based access control.
- Endpoint protection.
- Audit-log structure.
- Version history.
- Integrity mechanisms and threat assumptions.

### 4.10 Deployment and operations [H]

- Container structure.
- Local orchestration and service discovery.
- Kubernetes resources, if used.
- Secrets and configuration.
- Persistent storage.
- CI/CD pipeline.
- Monitoring and logging.
- Backups and restoration.
- Update and rollback strategy.
- Cost and resource considerations.

### 4.11 Testing concept and traceability implementation [W]

- Test levels and their purposes.
- Requirement-to-test mapping.
- Test data management.
- Reproducibility of measurement experiments.
- Separation of development tests from final evaluation.

---

## 5. Evaluation

Expected length: 20–30 pages

### 5.1 Evaluation environment and methodology [W]

- Hardware and software configuration.
- Versions of relevant libraries and models.
- Test objects and image dataset.
- Reference measurement equipment.
- Test participants, if usability testing is performed.
- Evaluation period and reproducibility information.
- Threats to validity.

### 5.2 Project milestones and development process [W]

- Initial requirements and planning.
- Architecture and technology decisions.
- First functional prototype.
- Provenance model implementation.
- Camera integration.
- Search implementation.
- Image similarity integration.
- Testing and refinement.
- Final deployment and documentation.

A milestone table should contain at least:

| Milestone | Planned date | Actual date | Result | Deviation and reason |
|---|---:|---:|---|---|
| Requirements completed | To be filled in | To be filled in | To be filled in | To be filled in |
| Architecture selected | To be filled in | To be filled in | To be filled in | To be filled in |
| Core object management implemented | To be filled in | To be filled in | To be filled in | To be filled in |
| Provenance model integrated | To be filled in | To be filled in | To be filled in | To be filled in |
| Depth-camera prototype completed | To be filled in | To be filled in | To be filled in | To be filled in |
| Image similarity prototype completed | To be filled in | To be filled in | To be filled in | To be filled in |
| Evaluation completed | To be filled in | To be filled in | To be filled in | To be filled in |

### 5.3 Evaluation of provenance-data modelling [H]

- Coverage of required object and provenance information.
- Ability to represent agents, events, places, sources and media.
- Handling of uncertainty and missing information.
- Consistency and validation results.
- Interoperability considerations.
- Implementation effort and maintainability.
- Remaining gaps compared with the selected standards.

### 5.4 Evaluation of depth-camera measurement [H]

#### 5.4.1 Experimental setup

- Camera placement and distance.
- Background and lighting.
- Object material and geometry.
- Reference dimensions.
- Number of repeated measurements.
- Measurement procedure.

#### 5.4.2 Metrics

- Absolute error.
- Relative error.
- Mean and median deviation.
- Standard deviation.
- Repeatability.
- Rate of invalid or unusable measurements.

#### 5.4.3 Results

Present results separately for different object categories and measurement conditions. Do not generalize a value measured on one object to all historical objects.

#### 5.4.4 Interpretation

- Conditions under which the camera is useful.
- Conditions under which manual verification remains necessary.
- Influence of material, distance, lighting and geometry.
- Suitability for ArtAdmin’s intended workflow.

### 5.5 Evaluation of image similarity and duplicate detection [W]

#### 5.5.1 Dataset construction

- Number of objects and images.
- Genuine duplicates or near duplicates.
- Similar but distinct objects.
- Variation in perspective, lighting, background, crop and image quality.
- Train, validation and test separation, if a trainable model is used.

#### 5.5.2 Metrics

- Precision.
- Recall.
- F1-score.
- False-positive rate.
- False-negative rate.
- Top-k retrieval accuracy, if applicable.
- Response time and resource consumption, if relevant.

#### 5.5.3 Threshold evaluation

- Definition of categories such as identical, possible duplicate, similar and not similar.
- Threshold selection procedure.
- Role of manual confirmation.

#### 5.5.4 Practical usability

- Whether users can understand similarity scores.
- Whether the results support real collection workflows.
- Cases where metadata or full-text search improves the result.

### 5.6 Evaluation of search and application functionality [H]

- Search correctness.
- Filtering and sorting.
- API response behaviour.
- Validation and error handling.
- Authentication and authorization tests.
- Media and measurement-data persistence.
- Requirement coverage.

### 5.7 Usability and workflow evaluation [W]

- Selection and description of participants.
- Moderated or unmoderated test method.
- Use cases given to participants.
- Task completion rate.
- Critical and non-critical errors.
- Observed misunderstandings.
- Feedback and resulting improvements.

### 5.8 Performance and operational evaluation [H]

- Search latency.
- Image-processing latency.
- Measurement workflow latency.
- Resource consumption.
- Startup and deployment behaviour.
- Backup and recovery test results, if performed.

### 5.9 Lessons learned [W,H]

- Technical knowledge gained.
- Experience with provenance modelling and cultural-heritage requirements.
- Experience with depth-camera measurement and experimental design.
- Experience with image similarity and threshold selection.
- Experience with frontend/backend integration.
- Experience with Git, issue tracking, code reviews and collaborative work.
- Experience with documentation and communication with the project partner.

### 5.10 What would be done differently [W,H]

- Decisions that could have been made earlier.
- Assumptions that required revision.
- Tests that should have been planned earlier.
- Data or hardware limitations.
- Improvements to project coordination and division of work.

### 5.11 Limitations and threats to validity [W]

- Limited number and diversity of test objects.
- Possible bias in the image dataset.
- Reference-measurement uncertainty.
- Dependence on environmental conditions.
- Limited generalizability of results.
- Dependence on third-party libraries, models and hardware.
- Difference between a prototype and production-grade collection software.

---

## 6. References, Literature and Figure Lists

This chapter follows the structure used in the provided example thesis, but the source quality requirements for ArtAdmin are stricter.

### 6.1 Scientific and technical references

Use a consistent citation style selected with the supervisor. Each entry should contain, where available:

- author or responsible organization;
- complete title;
- publication year;
- journal, conference, book or standard;
- publisher;
- DOI or stable official URL;
- access date for web-based documentation where required.

Priority sources include:

- official W3C PROV specifications;
- CIDOC and ICOM standards;
- LIDO documentation;
- official SPECTRUM documentation;
- peer-reviewed publications in cultural-heritage informatics;
- peer-reviewed depth-camera and 3D-measurement studies;
- IEEE, ACM, Springer, Elsevier and ISPRS publications;
- official Intel RealSense and librealsense documentation for implementation-specific facts.

Vendor documentation and project repositories are not peer-reviewed. They may be cited for API or hardware specifications, but this status should be made explicit.

### 6.2 Online sources and software documentation

- Official documentation for Angular, ASP.NET Core, PostgreSQL, Elasticsearch, Docker, Kubernetes and the selected identity provider.
- RealSense D456 documentation and librealsense repository.
- Only use online sources where they directly document a version-specific technical fact or standard.

### 6.3 Figure index

- Figure number.
- Caption.
- Page number.
- Source or author indication.

Figures created by the authors should be marked accordingly. Adapted figures require a source citation.

### 6.4 Table index

- Table number.
- Caption.
- Page number.

---

## Appendices

The appendices contain material that is important for verification but would interrupt the main argument.

### Appendix A – Decision matrices

- Provenance standards.
- Depth-camera and 3D-capture alternatives.
- Image-similarity methods.
- Search technologies.
- Deployment and authentication alternatives.

### Appendix B – Data model and standard mapping

- Complete entity-relationship diagram.
- Mapping to W3C PROV concepts.
- Mapping to CIDOC CRM and LIDO concepts where used.
- Controlled vocabularies and value definitions.

### Appendix C – API documentation

- OpenAPI extract or complete specification.
- Endpoint overview.
- Authentication requirements.
- Example request and response structures.

### Appendix D – System and deployment documentation

- Component and deployment diagrams.
- Container and orchestration configurations.
- CI/CD pipeline overview.
- Environment configuration description.

Do not include secrets, private keys or confidential credentials.

### Appendix E – Search and similarity configuration

- Search mappings.
- Similarity-index structure.
- Threshold-selection tables.
- Additional result examples.

### Appendix F – Measurement protocols and raw results

- Camera setup.
- Reference measurements.
- Environmental conditions.
- Repeated measurements.
- Raw depth-data references.
- Error calculations.

### Appendix G – Test cases and complete results

- Unit, integration and end-to-end test cases.
- Search tests.
- Image-similarity tests.
- Measurement tests.
- Usability-test protocols.

### Appendix H – User guide and interface screenshots

- Main workflows.
- User instructions.
- Validation and error messages.
- Screenshots with captions.

### Appendix I – Glossary and abbreviations

- Technical terms.
- Domain-specific cultural-heritage terminology.
- Abbreviations used in the thesis.