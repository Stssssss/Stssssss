## Hi there 👋

public class SelfIntroduction {
    public static void main(String[] args) {
        final String RESET = "\u001B[0m";
        final String CYAN = "\u001B[36m";
        final String GREEN = "\u001B[32m";
        final String YELLOW = "\u001B[33m";
        final String BLUE = "\u001B[34m";
        final String PURPLE = "\u001B[35m";
        final String RED = "\u001B[31m";
        final String BOLD = "\u001B[1m";
        
        System.out.println(CYAN + "╔═══════════════════════════════════════════════════╗" + RESET);
        System.out.println(CYAN + "║" + BOLD + "                SELF INTRODUCTION                " + RESET + CYAN + "║" + RESET);
        System.out.println(CYAN + "╠═══════════════════════════════════════════════════╣" + RESET);
        System.out.println(CYAN + "║ " + GREEN + "• Name: " + RESET + "Stsssss" + " ".repeat(35) + CYAN + "║" + RESET);
        System.out.println(CYAN + "║ " + GREEN + "• Occupation: " + RESET + "High School Student" + " ".repeat(22) + CYAN + "║" + RESET);
        System.out.println(CYAN + "║ " + GREEN + "• Mobile: " + RESET + "OnePlus 13" + " ".repeat(32) + CYAN + "║" + RESET);
        System.out.println(CYAN + "║ " + GREEN + "• Laptop: " + RESET + "Lenovo Legion Y7000p" + " ".repeat(23) + CYAN + "║" + RESET);
        System.out.println(CYAN + "╠═══════════════════════════════════════════════════╣" + RESET);
        System.out.println(CYAN + "║" + BOLD + "               TECHNICAL SKILLSET               " + RESET + CYAN + "║" + RESET);
        System.out.println(CYAN + "╠═══════════════════════════════════════════════════╣" + RESET);
        
        printSkill("Java", 80, BLUE);
        printSkill("Go", 75, CYAN);
        printSkill("Python", 70, YELLOW);
        printSkill("C/C++", 30, PURPLE);
        printSkill("Shell", 90, GREEN);
        
        System.out.println(CYAN + "╚═══════════════════════════════════════════════════╝" + RESET);
    }
    
    private static void printSkill(String name, int percentage, String color) {
        final String RESET = "\u001B[0m";
        final String CYAN = "\u001B[36m";
        
        int bars = (int) (percentage / 100.0 * 20);
        String progressBar = color + "█".repeat(bars) + RESET + "░".repeat(20 - bars);
        
        String percentageText = String.format("%3d%%", percentage);
        String skillText = String.format(CYAN + "║ " + RESET + "%-8s: %s %s" + " ".repeat(5) + CYAN + "║" + RESET, 
                                       name, progressBar, percentageText);
        
        System.out.println(skillText);
    }
}
