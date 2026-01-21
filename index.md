---
layout: default
title: Home
---

<header>
    <div class="container">
        <h1>Meditation Research @SLIM</h1>
        <p>Exploring Neural Mechanisms of Contemplative Practices</p>
        <div class="university">Michigan State University</div>
    </div>
</header>

<div class="container">
    <section id="about">
        <h2>About Our Research</h2>
        <p>Our interdisciplinary research group combines computational neuroscience, psychology, and biomedical engineering to understand the neural mechanisms underlying meditation practices. Using advanced EEG analysis and machine learning techniques, we investigate how different meditation techniques—particularly mantra-based practices—affect brain oscillations, cognitive performance, and mental well-being.</p>
        <p style="margin-top: 20px;">We maintain an in-house EEGlab facility equipped with state-of-the-art 64-channel wireless EEG systems, enabling longitudinal studies that track neural changes over weeks of meditation practice.</p>
    </section>



    <section id="research">
        <h2>Research Areas</h2>
        <div class="research-areas">
            <div class="research-card">
                <h4>Neural Mechanisms of Meditation</h4>
                <p>Investigating the brain dynamics underlying Japa meditation techniques, including mantra-based practices (Hare Krishna, Sa Ta Na Ma) and breath-focused meditation. Using advanced spectral analysis and FOOOF decomposition to identify neural biomarkers of meditation states.</p>
            </div>
            
            <div class="research-card">
                <h4>Cognitive & Behavioral Changes</h4>
                <p>Examining longitudinal improvements in attention, cognitive processing speed (P300 latency), mindfulness, interoceptive awareness, and stress reduction through controlled meditation interventions lasting 6+ weeks.</p>
            </div>
            
            <div class="research-card">
                <h4>Clinical Collaboration</h4>
                <p>Partnering with Henry Ford Hospital to develop advanced EEG-based methods for detecting and localizing epileptic activity in brain regions, applying our signal processing expertise to clinical challenges.</p>
            </div>
        </div>

        <h3 style="margin-top: 50px;">Key Findings</h3>
        <ul style="margin-left: 30px; margin-top: 20px;">
            <li>Mantra-based meditation produces distinct alpha band modulations compared to breath-focused techniques</li>
            <li>Six weeks of daily practice significantly reduces P300 latency, indicating improved neural processing efficiency</li>
            <li>Meditation enhances interoceptive awareness (MAIA scores) across all technique types</li>
            <li>Individual Alpha Frequency (IAF) increases and Individual Alpha Power (IAP) decreases during meditation, suggesting enhanced attentional control</li>
            <li>Deep learning models with Stationary Wavelet Transform modules successfully classify meditation states with >90% accuracy</li>
        </ul>
    </section>

    <section id="gallery">
        <h2>📸 Gallery: Talks & Presentations</h2>
        <p>Highlights from our conference presentations, research talks, and community outreach events.</p>
        
        <div class="gallery-grid">
            {% if site.data.gallery %}
                {% for item in site.data.gallery %}
                <div class="gallery-item" onclick="openLightbox('{{ item.image | relative_url }}')">
                    <img src="{{ item.image | relative_url }}" alt="{{ item.title }}">
                    <div class="gallery-caption">
                        <h4>{{ item.title }}</h4>
                        <p>{{ item.description }}</p>
                    </div>
                </div>
                {% endfor %}
            {% else %}
            <!-- Placeholder -->
            <div class="gallery-item">
                <div class="gallery-placeholder">📷</div>
                <div class="gallery-caption">
                    <h4>Conference Presentation</h4>
                    <p>Presenting findings at SfN conferences</p>
                </div>
            </div>
            
            <div class="gallery-item">
                <div class="gallery-placeholder">📷</div>
                <div class="gallery-caption">
                    <h4>EEG Lab Session</h4>
                    <p>Team conducting meditation EEG data collection</p>
                </div>
            </div>
            
            <div class="gallery-item">
                <div class="gallery-placeholder">📷</div>
                <div class="gallery-caption">
                    <h4>Poster Session</h4>
                    <p>International Neuroscience Conference</p>
                </div>
            </div>
            {% endif %}
        </div>
        
        <p style="margin-top: 30px; text-align: center; color: #666;">
            <em>Want to share photos from our events? Contact us at <a href="mailto:{{ site.email }}">{{ site.email }}</a></em>
        </p>
    </section>

    <section id="team">
        <h2>Research Team</h2>
        
        <h3>Lead Researchers</h3>
        <div class="team-grid">
            {% assign lead_researchers = site.data.team | where: "category", "Lead Researcher" %}
            {% for member in lead_researchers %}
            <div class="team-member">
                <h4>{{ member.name }}</h4>
                <div class="role">{{ member.role }}</div>
                <p>{{ member.department }}</p>
            </div>
            {% endfor %}
        </div>

        <h3>Advisory Faculty</h3>
        <div class="team-grid">
            {% assign advisors = site.data.team | where: "category", "Advisory Faculty" %}
            {% for member in advisors %}
            <div class="team-member">
                <h4>{{ member.name }}</h4>
                <div class="role">{{ member.role }}</div>
                <p>{{ member.department }}</p>
            </div>
            {% endfor %}
        </div>

        <h3>Research Support & Students</h3>
        <div class="team-grid">
            {% assign support = site.data.team | where: "category", "Research Support" %}
            {% for member in support %}
            <div class="team-member">
                <h4>{{ member.name }}</h4>
                <div class="role">{{ member.role }}</div>
                <p>{{ member.department }}</p>
            </div>
            {% endfor %}
        </div>

        <p style="margin-top: 30px;"><em>We also gratefully acknowledge our expert meditation instructors Devin O'Rourke (Harmony Collective) and our dedicated data collectors including Pratham Pradhan, Annie Wozniak, Vu Song Thuy Nguyen, Wei-ting Tan, Alisia Coipel, and Genevieve Orlewicz.</em></p>
    </section>

    <section id="publications">
        <h2>Selected Publications</h2>
        <ul class="publications">
            {% assign sorted_pubs = site.data.publications | sort: 'year' | reverse %}
            {% for pub in sorted_pubs %}
            <li>
                <strong>{{ pub.authors }}</strong> ({{ pub.year }}). "{{ pub.title }}" <em>{{ pub.venue }}.</em>
                {% if pub.pdf %}
                <br><a href="{{ pub.pdf | relative_url }}" target="_blank">📄 View Poster (PDF)</a>
                {% endif %}
                {% if pub.link %}
                <br><a href="{{ pub.link }}" target="_blank">🔗 Link</a>
                {% endif %}
            </li>
            {% endfor %}
        </ul>
        <p style="margin-top: 30px;"><em>Additional research supported by Brainwave Science, Inc. and collaborations with Brunel University London.</em></p>
    </section>

    <div class="opportunities">
        <h2 style="color: #ff6600; border-color: #ff6600;">🎓 Join Our Team</h2>
        
        <div class="opportunity-box">
            <h3>PhD Student Positions Available</h3>
            <p><strong>We are actively seeking motivated PhD students</strong> to join our research group. Ideal candidates will have:</p>
            <ul style="margin: 15px 0 15px 30px;">
                <li>Background in neuroscience, computational science, biomedical engineering, or related fields</li>
                <li>Interest in meditation research and contemplative neuroscience</li>
                <li>Experience with signal processing, machine learning, or EEG analysis (preferred but not required)</li>
                <li>Strong programming skills (Python, MATLAB)</li>
            </ul>
            <p><strong>What we offer:</strong> Opportunities to work on cutting-edge longitudinal meditation studies, collaborate with clinical partners, publish in top-tier journals, and contribute to a growing field of contemplative neuroscience.</p>
            <a href="mailto:{{ site.email }}" class="btn btn-secondary">Apply for PhD Position</a>
        </div>

        <div class="opportunity-box">
            <h3>Summer Research Internships</h3>
            <p><strong>Undergraduate and Master's students</strong> are invited to apply for summer research internships. This is an excellent opportunity to:</p>
            <ul style="margin: 15px 0 15px 30px;">
                <li>Gain hands-on experience with EEG data collection and analysis</li>
                <li>Learn advanced signal processing and machine learning techniques</li>
                <li>Contribute to ongoing meditation neuroscience studies</li>
                <li>Co-author research publications and conference presentations</li>
            </ul>
            <p><strong>Duration:</strong> 8-12 weeks during summer<br>
            <strong>Eligibility:</strong> Current undergraduate or Master's students in relevant fields</p>
            <a href="mailto:{{ site.email }}" class="btn btn-secondary">Apply for Summer Internship</a>
        </div>
    </div>

    <section id="contact">
        <h2>Contact Us</h2>
        <div class="contact-info">
            <p><strong>For PhD positions, internships, or collaboration inquiries:</strong></p>
            <p>Email: <a href="mailto:{{ site.email }}">{{ site.email }}</a></p>
            <p>Department of Computational Mathematics, Science and Engineering<br>
            Michigan State University<br>
            East Lansing, MI 48824</p>
        </div>
    </section>
</div>

<!-- Lightbox Modal -->
<div id="lightbox" class="lightbox" onclick="closeLightbox()">
    <span class="lightbox-close">&times;</span>
    <img class="lightbox-content" id="lightbox-img">
</div>