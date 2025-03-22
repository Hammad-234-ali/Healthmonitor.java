# Healthmonitor.java
import java.util.ArrayList;
import java.util.List;

class HealthMonitor {
    private List<String> physicalIssues;
    private List<String> mentalIssues;

    public HealthMonitor() {
        this.physicalIssues = new ArrayList<>();
        this.mentalIssues = new ArrayList<>();
    }

    public void detectPhysicalIssues(int screenTime) {
        if (screenTime > 180) {
            physicalIssues.add("Eye Strain");
            physicalIssues.add("Back Pain");
        }
    }

    public void detectMentalIssues(int stressLevel) {
        if (stressLevel > 5) {
            mentalIssues.add("High Stress");
        }
    }

    public void provideSuggestions() {
        System.out.println("Physical Issues: " + physicalIssues);
        System.out.println("Mental Issues: " + mentalIssues);
    }
}
