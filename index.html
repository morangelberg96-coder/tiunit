// ============================================================
// כתיבה טיעונית – שיטת פטנד"ס
// יצרה וערכה בעזרת בינה מלאכותית: מורן קמיל גלברג – הוראה מותאמת
// ============================================================

import { useState, useEffect, useRef, useCallback } from "react";

// ==================== DATA ====================

const TOPICS = [
  { id: 1, title: "האם יש לאסור שימוש בטלפונים ניידים בבתי ספר?", short: "טלפונים בבתי ספר" },
  { id: 2, title: "האם יש להנהיג מדי בית ספר אחידים?", short: "מדי בית ספר" },
  { id: 3, title: "האם יש להאריך את שנת הלימודים?", short: "הארכת שנת הלימודים" },
  { id: 4, title: "האם יש לבטל את שיעורי הבית?", short: "ביטול שיעורי בית" },
  { id: 5, title: "האם יש להוריד את גיל ההצבעה ל-16?", short: "גיל הצבעה" },
  { id: 6, title: "האם יש להגביל את השימוש ברשתות חברתיות לבני נוער?", short: "רשתות חברתיות" },
  { id: 7, title: "האם על בני נוער לעבוד בעבודות קיץ?", short: "עבודות קיץ" },
  { id: 8, title: "האם יש להכניס שיעורי חינוך פיננסי כחובה בבתי ספר?", short: "חינוך פיננסי" },
  { id: 9, title: "האם יש לעודד שירות לאומי-אזרחי לכל בני הנוער?", short: "שירות לאומי" },
  { id: 10, title: "האם יש לאפשר לתלמידים לבחור את המקצועות שהם לומדים?", short: "בחירת מקצועות" },
  { id: 11, title: "האם יש להחליף מבחנים בהערכה חלופית?", short: "הערכה חלופית" },
  { id: 12, title: "האם בינה מלאכותית מועילה או מזיקה לתלמידים?", short: "בינה מלאכותית" },
  { id: "custom", title: "נושא חופשי – אני רוצה לבחור נושא משלי!", short: "נושא חופשי" },
];

const OPENING_STYLES = [
  {
    name: "פתיחה בשאלה רטורית", icon: "❓",
    description: "פתיחה בשאלה שאינה דורשת תשובה אלא מעוררת חשיבה",
    example: "האם אי פעם חשבתם כמה שעות ביום אתם מבלים מול המסך של הטלפון הנייד? נושא השימוש בטלפונים ניידים מעסיק רבים בימינו.",
    template: "האם אי פעם חשבתם...? נושא זה מעסיק רבים...",
  },
  {
    name: "פתיחה בציטוט או פתגם", icon: "💬",
    description: "שימוש בציטוט מוכר או פתגם שקשור לנושא",
    example: '"החינוך הוא הנשק החזק ביותר שאפשר להשתמש בו כדי לשנות את העולם" – נלסון מנדלה. נושא החינוך מעסיק רבים, ואחד הנושאים השנויים במחלוקת הוא...',
    template: '"..." – אמר/ה... נושא זה מעלה שאלות רבות בנוגע ל...',
  },
  {
    name: "פתיחה בנתון או עובדה", icon: "📊",
    description: "הצגת נתון מפתיע או עובדה מעניינת הקשורה לנושא",
    example: "על פי מחקר שנערך לאחרונה, כ-90% מבני הנוער משתמשים בטלפון הנייד במהלך שעות הלימודים. נתון זה מעלה שאלות לגבי מקומו של הטלפון בכיתה.",
    template: "על פי מחקר/סקר... נתון זה מעלה את השאלה...",
  },
  {
    name: "פתיחה בסיפור קצר", icon: "📖",
    description: "סיפור קצר או מקרה שקרה שקשור לנושא",
    example: "דני, תלמיד כיתה ח', ישב בשיעור מתמטיקה כשפתאום הטלפון שלו צלצל. כל הכיתה צחקה, והמורה כעסה. מקרים כאלה מתרחשים מדי יום בבתי ספר רבים.",
    template: "...ישב/ה ב... כש... מקרים כאלה מעלים את השאלה...",
  },
  {
    name: "פתיחה כללית בהצגת הנושא", icon: "🌐",
    description: "הצגה כללית של הנושא והרקע שלו",
    example: "נושא השימוש בטלפונים ניידים בבתי ספר נמצא על סדר היום הציבורי זה זמן רב. גורמים שונים חלוקים בדעותיהם בנושא זה.",
    template: "נושא... נמצא על סדר היום... גורמים שונים חלוקים בדעותיהם...",
  },
];

const CONNECTOR_WORDS = {
  opening: ["בימינו,", "בעידן המודרני,", "מאז ומעולם,", "לאחרונה,", "זה זמן רב ש..."],
  claim: ["לדעתי,", "אני סבור/ה ש...", "עמדתי היא ש...", "לאחר בחינת הנושא, אני טוען/ת ש..."],
  reason: ["מפני ש...", "משום ש...", "כיוון ש...", "הסיבה לכך היא ש...", "בשל העובדה ש..."],
  addition: ["נוסף על כך,", "יתרה מזו,", "זאת ועוד,", "כמו כן,", "בנוסף,"],
  beginning: ["ראשית,", "שנית,", "שלישית,", "לפני הכול,", "קודם כול,"],
  example: ["לדוגמה,", "כפי שניתן לראות...", "מחקרים מראים ש...", "למשל,"],
  refutation: ["אמנם יש הטוענים ש..., אולם...", "למרות הטענה ש..., יש לזכור ש...", "אף על פי ש..., בפועל...", "נכון ש..., אך..."],
  summary: ["לסיכום,", "לאור כל האמור לעיל,", "מכל הסיבות שהוזכרו,", "לאור האמור,"],
};

// ==================== QUIZ DATA ====================

const OPENING_QUIZ = [
  {
    text: "האם אי פעם חשבתם כמה זמן אתם מבלים מול מסכים? נושא זה מעסיק רבים.",
    isGood: true, explanation: "פתיחה מצוינת! שאלה רטורית שמעוררת חשיבה + הצגת הנושא כדילמה."
  },
  {
    text: "לדעתי, חייבים לאסור טלפונים בבתי ספר כי הם מזיקים.",
    isGood: false, explanation: "זו לא פתיחה טובה! הכותב חשף את דעתו כבר בפתיחה. הפתיחה צריכה להיות כללית ולא לחשוף עמדה."
  },
  {
    text: "נושא השימוש בטכנולוגיה בכיתה מעסיק מורים, הורים ותלמידים רבים. יש הטוענים שמדובר בכלי למידה חשוב, ויש הטוענים שהוא פוגע בריכוז.",
    isGood: true, explanation: "פתיחה מצוינת! מציגה את הנושא + דילמה ברורה (שני צדדים) בלי לגלות דעה."
  },
  {
    text: "טלפונים ניידים.",
    isGood: false, explanation: "זו לא פתיחה! זה רק נושא. פתיחה צריכה להציג את הנושא כדילמה ולעורר עניין."
  },
  {
    text: "כולם יודעים שמדים זה רעיון גרוע ואף אחד לא אוהב אותם.",
    isGood: false, explanation: "פתיחה בעייתית! הכותב חושף דעה חד-משמעית ומכליל ('כולם', 'אף אחד')."
  },
  {
    text: "על פי סקר שנערך בקרב בני נוער בישראל, 78% מהם מעדיפים לבחור את הלבוש שלהם. נתון זה מעלה שאלה חשובה בנוגע למדי בית ספר.",
    isGood: true, explanation: "פתיחה מצוינת! נתון מעניין + שאלה/דילמה ('מעלה שאלה חשובה')."
  },
  {
    text: "בימינו יש טלפונים ניידים. הם קיימים כבר שנים רבות ואנשים רבים משתמשים בהם.",
    isGood: false, explanation: "הפתיחה מציגה את הנושא, אבל חסרה דילמה! אין שאלה, ויכוח או התלבטות. הקורא לא מבין שיש על מה לדון."
  },
];

const CLAIM_QUIZ = [
  {
    text: "לדעתי, יש לאסור את השימוש בטלפונים ניידים בבתי ספר.",
    isGood: true, explanation: "טענה מצוינת! ברורה, חד-משמעית, מביעה עמדה ברורה."
  },
  {
    text: "טלפונים ניידים זה נושא מעניין.",
    isGood: false, explanation: "זו לא טענה! אין כאן הבעת עמדה בעד או נגד."
  },
  {
    text: "אני חושב שאולי יכול להיות שמדים זה לא רעיון כל כך טוב, אבל גם לא רע.",
    isGood: false, explanation: "טענה חלשה! לא ברורה, מלאה בהססנות. טענה צריכה להיות נחרצת וברורה."
  },
  {
    text: "עמדתי היא שיש להכניס שיעורי חינוך פיננסי כחובה בכל בתי הספר.",
    isGood: true, explanation: "טענה מצוינת! ברורה, נחרצת, וניתן לתמוך בה בנימוקים."
  },
  {
    text: "שיעורי בית זה משעמם.",
    isGood: false, explanation: "זו לא טענה טובה! זו סתם הבעת רגש בלי טענה ברורה אם לבטל או לא."
  },
];

const ARGUMENT_QUIZ_DATA = {
  claim: "יש לאסור שימוש בטלפונים ניידים בבתי ספר",
  arguments: [
    { text: "טלפונים ניידים מסיחים את דעת התלמידים מהלמידה ופוגעים בריכוז", supports: true, explanation: "נימוק תומך! מסביר למה צריך לאסור – כי זה פוגע בלמידה." },
    { text: "טלפונים ניידים הם כלי תקשורת חשוב", supports: false, explanation: "נימוק שלא תומך בטענה! זהו נימוק בעד טלפונים, לא נגדם." },
    { text: "ללא טלפונים, התלמידים ישתתפו יותר בשיעורים ויפתחו קשרים חברתיים אמיתיים", supports: true, explanation: "נימוק תומך! מסביר את היתרון של האיסור." },
    { text: "יש אפליקציות לימודיות שימושיות בטלפון", supports: false, explanation: "נימוק שלא תומך! מדבר על יתרון של טלפונים – ההפך מהטענה." },
    { text: "שימוש בטלפון בזמן השיעור עלול להוביל לבריונות רשת ולפגיעה בתלמידים", supports: true, explanation: "נימוק תומך! מציג סכנה שנימנעת על ידי האיסור." },
    { text: "הפיצה בבית הספר טעימה", supports: false, explanation: "נימוק לא קשור כלל לנושא!" },
  ]
};

const CONNECTOR_QUIZ = [
  { word: "ראשית,", category: "beginning", categoryName: "התחלה/סדר" },
  { word: "מפני ש...", category: "reason", categoryName: "סיבה" },
  { word: "נוסף על כך,", category: "addition", categoryName: "הוספה" },
  { word: "לסיכום,", category: "summary", categoryName: "סיכום" },
  { word: "שנית,", category: "beginning", categoryName: "התחלה/סדר" },
  { word: "כיוון ש...", category: "reason", categoryName: "סיבה" },
  { word: "זאת ועוד,", category: "addition", categoryName: "הוספה" },
  { word: "לאור כל האמור,", category: "summary", categoryName: "סיכום" },
  { word: "משום ש...", category: "reason", categoryName: "סיבה" },
  { word: "כמו כן,", category: "addition", categoryName: "הוספה" },
  { word: "שלישית,", category: "beginning", categoryName: "התחלה/סדר" },
  { word: "מכל הסיבות שהוזכרו,", category: "summary", categoryName: "סיכום" },
];

const REFUTATION_EXERCISES = [
  {
    topic: "האם יש לאסור שימוש בטלפונים ניידים בבתי ספר?",
    claim: "יש לאסור שימוש בטלפונים ניידים בבתי ספר",
    argument: "טלפונים ניידים מפריעים לריכוז בשיעורים",
    refutationHint: "חשבו: האם אפשר להשתמש בטלפון ככלי לימודי?",
    exampleRefutation: "אמנם יש הטוענים שטלפונים ניידים מפריעים לריכוז, אולם ניתן להשתמש בהם ככלי לימודי יעיל – לחיפוש מידע, לתרגול באפליקציות חינוכיות ולשיתוף פעולה.",
  },
  {
    topic: "האם יש להנהיג מדי בית ספר אחידים?",
    claim: "יש להנהיג מדי בית ספר אחידים",
    argument: "מדים אחידים מבטלים את הביטוי האישי של התלמידים",
    refutationHint: "חשבו: האם יש דרכים אחרות לבטא את עצמך מלבד לבוש?",
    exampleRefutation: "אמנם יש הטוענים שמדים מבטלים את הביטוי האישי, אולם ביטוי אישי אינו מוגבל ללבוש בלבד – תלמידים יכולים לבטא את עצמם דרך יצירתיות, כתיבה, ספורט ותחביבים.",
  },
  {
    topic: "האם יש לבטל את שיעורי הבית?",
    claim: "יש לבטל את שיעורי הבית",
    argument: "שיעורי בית עוזרים לחזק את החומר הנלמד",
    refutationHint: "חשבו: האם יש דרכים אחרות לחזק את החומר?",
    exampleRefutation: "אמנם יש הטוענים ששיעורי בית מחזקים את הלמידה, אולם מחקרים מראים שתרגול בכיתה בליווי המורה יעיל יותר מתרגול עצמאי בבית.",
  },
];

// ==================== AI FEEDBACK ====================

function getRuleBasedFeedback(section, content, topic, claim, side) {
  const text = (content || "").trim();
  const wordCount = text.split(/\s+/).filter(w => w.length > 0).length;
  
  if (!text || wordCount < 3) {
    return "✏️ נראה שעדיין לא כתבתם מספיק. נסו לכתוב לפחות משפט או שניים כדי שאוכל לתת משוב!";
  }
  
  const isGibberish = /^[אבגדהוזחטיכלמנסעפצקרשת\s]{1,10}$/.test(text) || 
    /בלה\s*בלה/i.test(text) || /אאא|בבב|גגג/.test(text) ||
    wordCount < 3;

  if (isGibberish) {
    return "🤔 נראה שהטקסט עדיין לא מוכן לבדיקה. נסו לכתוב תוכן אמיתי – אפילו משפט פשוט אחד – ואז אבדוק שוב!";
  }

  const feedbacks = [];
  
  // Sentence quality checks
  const endsWithPeriod = /[.!?।]$/.test(text.trim());
  const hasVerb = /[אבגדהוזחטיכלמנסעפצקרשת]{2,}(ים|ות|ה|ת|תי|נו|תם|תן|ו|י)\b/.test(text);
  const sentences = text.split(/[.!?]/).filter(s => s.trim().length > 3);
  const avgWordsPerSentence = sentences.length > 0 ? wordCount / sentences.length : wordCount;
  const isFragment = wordCount < 6 && !endsWithPeriod;
  const isPartialSentence = wordCount >= 3 && wordCount < 8 && !endsWithPeriod;
  const lacksDepth = wordCount < 12;
  
  // === INCOMPLETE SENTENCE DETECTION ===
  // Check if sentence trails off / is cut mid-thought
  const trailingWords = /\s(גם|ש|כי|אבל|מפני ש|בגלל ש|כמו|על ידי|כדי ש|בזכות|בשל|למרות ש|אף על פי ש|כגון|כפי ש|לפי|עקב|בעקבות|משום ש|הודות ל|ניתן ל|אפשר ל|צריך ל|כמו כן|בנוסף|וגם|אלא|אולם|לכן|ולכן)\s*[.!?]?\s*$/;
  const hasTrailing = trailingWords.test(text.trim());
  
  // Check for sentences within the text that trail off (split by period)
  const incompleteSentences = [];
  const allSentences = text.split(/[.!?]/).map(s => s.trim()).filter(s => s.length > 5);
  allSentences.forEach(s => {
    if (trailingWords.test(s)) {
      incompleteSentences.push(s);
    }
  });
  // Also check the very last part (might not end with punctuation)
  const lastPart = text.trim().replace(/[.!?]\s*$/, "").split(/[.!?]/).pop()?.trim() || "";
  if (lastPart.length > 5 && trailingWords.test(lastPart) && !incompleteSentences.includes(lastPart)) {
    incompleteSentences.push(lastPart);
  }
  
  // === GENERAL: Incomplete sentence check (applies to all sections) ===
  if (incompleteSentences.length > 0 && section !== "draft") {
    const firstIncomplete = incompleteSentences[0];
    const lastWord = firstIncomplete.trim().split(/\s+/).pop();
    feedbacks.push(`⚠️ יש משפט שנקטע באמצע! המשפט "...${firstIncomplete.slice(-40)}" לא מסתיים – מה רציתם לומר אחרי "${lastWord}"?`);
    feedbacks.push("📝 כל משפט חייב להיות שלם: להתחיל ברעיון, לפתח אותו, ולהגיע לסוף ברור עם נקודה.");
  }

  if (section === "opening") {
    // === SENTENCE QUALITY CHECKS FIRST - before anything else ===
    if (isFragment) {
      feedbacks.push("⚠️ מה שכתבתם הוא לא משפט שלם! פתיחה צריכה להיות לפחות 2-3 משפטים שלמים שמציגים את הנושא.");
      feedbacks.push("📝 משפט שלם כולל: נושא + פועל + השלמה, ומסתיים בנקודה.");
      feedbacks.push("💡 דוגמה: 'בימינו, נושא הטלפונים הניידים מעסיק רבים. יש הטוענים שהם מפריעים ללמידה, ויש הטוענים שהם כלי חיוני.'");
      return feedbacks.join("\n");
    }
    
    if (isPartialSentence) {
      feedbacks.push("⚠️ המשפט שלכם לא שלם ולא ברור. חסרים חלקים חשובים כדי שהקורא יבין מה רציתם לומר.");
      feedbacks.push("📝 וודאו שיש: נושא (על מה מדברים) + פועל (מה קורה) + השלמה. סיימו בנקודה.");
      feedbacks.push("💡 דוגמה למשפט שלם: 'בשנים האחרונות, נושא שיעורי הבית עולה שוב ושוב לדיון ציבורי.'");
      return feedbacks.join("\n");
    }
    
    if (!endsWithPeriod && wordCount > 3) {
      feedbacks.push("⚠️ המשפט לא מסתיים בנקודה. כל משפט חייב להסתיים בנקודה, סימן שאלה או סימן קריאה.");
    }
    
    // === CONTENT RELEVANCE - is this actually an opening? ===
    const looksLikeClaim = /לדעתי|אני סבור|אני חושב|עמדתי|אני טוען/.test(text);
    const looksLikeArgument = /ראשית|שנית|מפני ש|כיוון ש|הסיבה היא/.test(text);
    const looksLikeSummary = /לסיכום|לאור כל|מכל הסיבות/.test(text);
    
    if (looksLikeClaim && !looksLikeArgument) {
      feedbacks.push("⚠️ נראה שכתבתם טענה ולא פתיחה! פתיחה מציגה את הנושא באופן ניטרלי, בלי לחשוף דעה. הטענה תבוא בשלב הבא.");
      return feedbacks.join("\n");
    }
    if (looksLikeSummary) {
      feedbacks.push("⚠️ זה נראה יותר כמו סיכום ולא כמו פתיחה! פתיחה מציגה את הנושא לראשונה, לא מסכמת אותו.");
      return feedbacks.join("\n");
    }
    
    if (lacksDepth) {
      feedbacks.push("✏️ הפתיחה קצרה מדי. פתיחה טובה כוללת לפחות 2-3 משפטים שמציגים את הנושא ומעוררים עניין.");
    }
    
    // === ONLY NOW check content quality ===
    // Opinion detection - smart: distinguishes questions/dilemmas from actual opinions
    
    const hasOpinion = (() => {
      // Check if the text is framed as a question/dilemma - then opinion words are OK
      const isQuestionContext = /האם\s/.test(text) || /נשאלת השאלה/.test(text) || /עולה השאלה/.test(text) || /השאלה היא/.test(text) || /או לא\??/.test(text) || /או שלא/.test(text);
      
      // These are ALWAYS opinion (even inside questions): first person stance
      const strongOpinion = [
        /לדעתי/, /אני חושב[ת]?/, /אני סבור[ה]?/, /אני מאמין[ה]?/, /אני טוען[ת]?/,
        /עמדתי/, /אני בעד/, /אני נגד/, /אני תומך/, /אני מתנגד/,
        /נראה לי/, /נדמה לי/, /לטעמי/, /מבחינתי/, /בעיניי/,
        /אני מרגיש[ה]?/, /לפי דעתי/, /אני משוכנע/, /אני בטוח[ה]?/,
        /אני מעדיפ/, /הייתי רוצה/, /הייתי מעדיפ/,
        /ברור לי/, /ברור לנו/, /לענ"ד/, /לעניות דעתי/, /לפי השקפתי/,
      ];
      if (strongOpinion.some(p => p.test(text))) return true;
      
      // These trigger ONLY if NOT inside a question context
      if (!isQuestionContext) {
        const contextualOpinion = [
          /צריך ש/, /צריכים ל/, /חייבים ל/,
          /ברור ש/, /אין ספק/, /ללא ספק/, /ודאי ש/, /בוודאי/,
          /יש לאסור/, /יש לבטל/, /יש להנהיג/, /יש לאפשר/, /יש להכניס/,
          /יש לעודד/, /יש להגביל/, /יש להאריך/, /יש להוריד/, /יש להחליף/,
          /אסור ל/, /מומלץ ל/, /ראוי ל/, /עדיף ל/, /חשוב ש/, /הכרחי ש/,
          /כולם יודעים/, /אף אחד לא/,
          /זה טוב/, /זה רע/, /זה נכון/, /זה לא נכון/,
          /זה חשוב/, /זה מזיק/, /זה מועיל/,
          /זה רעיון טוב/, /זה רעיון גרוע/, /זה רעיון רע/, /זה רעיון מצוין/,
          /נראה שכן/, /נראה שלא/,
          /כן צריך/, /לא צריך/, /בהחלט כן/, /בהחלט לא/,
          /ממש לא/, /ממש כן/, /בטח ש/, /אני חש[ה]?/,
        ];
        if (contextualOpinion.some(p => p.test(text))) return true;
      }
      return false;
    })();
    const hasTopic = topic && text.length > 20;
    const hasQuestion = /\?/.test(text);
    const hasQuote = /["״"']/.test(text);
    const hasNumber = /\d+%|\d+ מ/.test(text);
    
    if (hasOpinion) {
      feedbacks.push("⚠️ שימו לב – נראה שהפתיחה שלכם חושפת את דעתכם! בפתיחה אנחנו עדיין לא חושפים עמדה. נסו לשכתב בלי מילים שמביעות עמדה.");
    } else if (wordCount >= 10 && endsWithPeriod) {
      feedbacks.push("👏 הפתיחה לא חושפת דעה – בדיוק כמו שצריך!");
    }
    
    if (hasQuestion) feedbacks.push("✨ שימוש יפה בשאלה!");
    if (hasQuote) feedbacks.push("💬 ציטוט זו דרך מעניינת לפתוח!");
    if (hasNumber) feedbacks.push("📊 שימוש בנתון – נותן אמינות!");
    
    // === DILEMMA / DELIBERATION CHECK ===
    const dilemmaPatterns = [
      /\?/, // question mark
      /האם/, /השאלה/, /הדילמה/, /ההתלבטות/, /הויכוח/, /הוויכוח/, /המחלוקת/,
      /יש הטוענים.*ויש/, /יש הסבורים.*ויש/, /יש האומרים.*ויש/,
      /מצד אחד.*מצד שני/,
      /חלק.*וחלק/, /יש.*ויש/,
      /תומכים.*מתנגדים/, /בעד.*נגד/,
      /חלוקות הדעות/, /דעות שונות/, /דעות חלוקות/,
      /נושא שנוי במחלוקת/, /סוגייה/, /שאלה/,
      /עולה לדיון/, /מעסיק/, /עולה שוב ושוב/,
      /לא פשוט/, /סוגיה מורכבת/, /נושא מורכב/,
    ];
    const hasDilemma = dilemmaPatterns.some(p => p.test(text));
    
    if (!hasDilemma && wordCount >= 10 && !hasOpinion) {
      feedbacks.push("💡 הפתיחה מציגה את הנושא, אבל חסרה **דילמה או שאלה**. פתיחה טובה מראה שיש התלבטות או ויכוח סביב הנושא.");
      feedbacks.push("📝 נסו להוסיף: שאלה ('האם...?'), או הצגת שני צדדים ('יש הטוענים... ויש הטוענים...'), או מילת דילמה ('הנושא שנוי במחלוקת').");
    } else if (hasDilemma && !hasOpinion && wordCount >= 10) {
      feedbacks.push("🌟 יש דילמה/שאלה בפתיחה – מצוין! זה מראה לקורא שיש מה לדון.");
    }
    
    if (wordCount >= 10 && wordCount < 18) {
      feedbacks.push("📝 אורך סביר, אבל אפשר להרחיב עוד קצת.");
    } else if (wordCount >= 18) {
      feedbacks.push("👍 אורך טוב לפתיחה!");
    }
    
    if (!hasOpinion && hasTopic && wordCount >= 10) {
      feedbacks.push("✅ הנושא מוצג בצורה ברורה.");
    }
  }
  
  else if (section === "claim") {
    const hasOpinionWord = /לדעתי|אני סבור|עמדתי|אני חושב|אני טוען|אני מאמין/.test(text);
    const hasClearStance = /יש ל|אין ל|צריך|ראוי ל|חייבים|מומלץ/.test(text);
    const isHesitant = /אולי|יכול להיות|לא בטוח|גם וגם|מצד אחד.*מצד שני/.test(text);
    
    if (isFragment) {
      feedbacks.push("⚠️ זה לא משפט שלם. טענה חייבת להיות משפט שלם עם נושא, פועל והשלמה.");
      feedbacks.push("💡 דוגמה: 'לדעתי, יש לאסור שימוש בטלפונים ניידים בבתי ספר.'");
      return feedbacks.join("\n");
    }
    
    if (isPartialSentence) {
      feedbacks.push("⚠️ המשפט לא שלם ולא ברור. חסרים חלקים כדי שהטענה תהיה מובנת.");
      feedbacks.push("📝 וודאו שהטענה כוללת: מילת דעה (לדעתי) + מה אתם חושבים + נקודה.");
      return feedbacks.join("\n");
    }
    
    if (!endsWithPeriod && wordCount > 3) {
      feedbacks.push("⚠️ סיימו את הטענה בנקודה.");
    }
    
    // Content relevance
    const looksLikeOpening = wordCount > 20 && !hasOpinionWord && !hasClearStance;
    if (looksLikeOpening) {
      feedbacks.push("⚠️ נראה שכתבתם פתיחה ולא טענה! טענה היא משפט קצר וברור שמביע דעה: 'לדעתי, יש ל...'");
      return feedbacks.join("\n");
    }
    
    if (isHesitant) {
      feedbacks.push("🤔 הטענה מהססת. טענה טובה היא נחרצת! השתמשו ב'לדעתי' ואמרו בבירור: בעד או נגד.");
    } else if (hasOpinionWord && hasClearStance) {
      feedbacks.push("🌟 טענה מצוינת! ברורה, נחרצת, ומביעה עמדה. כל הכבוד!");
    } else if (hasClearStance) {
      feedbacks.push("👍 יש עמדה ברורה. אפשר לחזק עם 'לדעתי' או 'עמדתי היא ש...'.");
    } else {
      feedbacks.push("⚠️ לא ברור מה העמדה שלכם. נסחו משפט שמתחיל ב'לדעתי, יש ל...' או 'לדעתי, אין ל...'");
    }
    
    if (wordCount > 30) {
      feedbacks.push("📏 הטענה ארוכה מדי. טענה טובה היא קצרה וממוקדת – משפט אחד.");
    }
  }
  
  else if (section === "arguments") {
    const hasExampleWords = /לדוגמה|למשל|מחקר|סקר|כפי ש|מראים/.test(text);
    const hasConnectors = /ראשית|שנית|נוסף על כך|יתרה מזו|זאת ועוד|כמו כן/.test(text);
    const hasReasonWords = /מפני|משום|כיוון|בשל|הסיבה/.test(text);
    
    // Check sentence completeness first
    if (isFragment) {
      feedbacks.push("⚠️ כתבתם רק רעיון כללי, לא נימוק מנוסח. נימוק צריך להיות משפט שלם שמסביר סיבה.");
      feedbacks.push("📝 משפט שלם = נושא + פועל + השלמה + נקודה.");
      feedbacks.push("💡 דוגמה: 'ראשית, שימוש בטלפונים פוגע בריכוז התלמידים, מפני שהתראות מסיחות את הדעת.'");
      return feedbacks.join("\n");
    }
    
    if (isPartialSentence) {
      feedbacks.push("⚠️ המשפט לא שלם. חסרים חלקים כדי שהנימוק יהיה ברור.");
      feedbacks.push("📝 נסו לכתוב משפט מלא שמסביר **למה** – לא רק מילה או רעיון.");
      return feedbacks.join("\n");
    }
    
    // Content relevance
    const looksLikeClaim = /לדעתי|אני סבור|עמדתי היא/.test(text) && wordCount < 15;
    if (looksLikeClaim) {
      feedbacks.push("⚠️ נראה שכתבתם טענה ולא נימוקים! נימוק הוא סיבה שתומכת בטענה, עם דוגמה. השתמשו ב'ראשית...', 'מפני ש...'.");
      return feedbacks.join("\n");
    }
    
    if (lacksDepth) {
      feedbacks.push("✏️ הנימוקים קצרים מדי. נסו לפתח כל נימוק – הסבירו למה הוא חשוב והוסיפו דוגמה ספציפית.");
    } else {
      feedbacks.push("👏 כתבתם נימוקים בהיקף טוב!");
    }
    
    if (!endsWithPeriod && wordCount > 5) {
      feedbacks.push("💡 שימו לב: כל משפט צריך להסתיים בנקודה.");
    }
    
    if (hasConnectors) {
      feedbacks.push("✨ שימוש יפה במילות קישור וסדר!");
    } else {
      feedbacks.push("💡 חסרות מילות קישור! הוסיפו 'ראשית', 'שנית', 'נוסף על כך' כדי ליצור סדר בין הנימוקים.");
    }
    
    if (hasExampleWords) {
      feedbacks.push("📚 יפה! הוספתם דוגמאות – זה מחזק את הנימוקים.");
    } else {
      feedbacks.push("📝 חסרות דוגמאות! הוסיפו 'לדוגמה...' או 'למשל...' כדי לחזק כל נימוק.");
    }
    
    if (hasReasonWords) {
      feedbacks.push("👍 שימוש טוב במילות סיבה!");
    } else if (wordCount > 15) {
      feedbacks.push("💡 נסו להוסיף מילות סיבה כמו 'מפני ש', 'כיוון ש' כדי להסביר למה.");
    }
  }
  
  else if (section === "summary") {
    const hasSummaryWord = /לסיכום|לאור|מכל|סוף דבר|לסיום/.test(text);
    const hasRecommendation = /ממליץ|מומלץ|כדאי|ראוי|יש ל|חשוב ש/.test(text);
    const hasConclusion = /לכן|על כן|מסקנ|נובע|עולה/.test(text);
    
    if (isFragment) {
      feedbacks.push("⚠️ זה לא משפט שלם. סיכום צריך לפחות 2-3 משפטים שלמים: חזרה על הטענה, מסקנה, והמלצה.");
      feedbacks.push("💡 דוגמה: 'לסיכום, לאור כל הנימוקים שהוצגו, יש לאסור טלפונים בבתי ספר. מומלץ שמשרד החינוך יקבע כללים ברורים.'");
      return feedbacks.join("\n");
    }
    
    if (isPartialSentence) {
      feedbacks.push("⚠️ המשפט לא שלם ולא ברור. וודאו שיש נושא, פועל, והשלמה. סיימו בנקודה.");
      return feedbacks.join("\n");
    }
    
    if (!endsWithPeriod && wordCount > 5) {
      feedbacks.push("⚠️ המשפט לא מסתיים בנקודה.");
    }
    
    // Content relevance
    const looksLikeOpening = !hasSummaryWord && !hasConclusion && !/לדעתי|עמדתי/.test(text) && wordCount > 15;
    const looksLikeNewArgument = /ראשית|שנית|נוסף על כך|מפני ש/.test(text) && !hasSummaryWord;
    if (looksLikeNewArgument) {
      feedbacks.push("⚠️ נראה שכתבתם נימוק חדש ולא סיכום! בסיכום לא מוסיפים נימוקים חדשים – אלא חוזרים על הטענה ומסיקים מסקנה.");
      return feedbacks.join("\n");
    }
    
    if (hasSummaryWord) {
      feedbacks.push("✅ פתחתם עם מילת סיכום – מצוין!");
    } else {
      feedbacks.push("⚠️ חסרה מילת סיכום! פתחו ב'לסיכום' או 'לאור כל האמור'.");
    }
    
    if (wordCount < 15) {
      feedbacks.push("✏️ הסיכום קצר. צריך לפחות 2-3 משפטים: חזרה על הטענה + מסקנה + המלצה.");
    }
    
    if (hasConclusion) {
      feedbacks.push("🎯 יפה! הסקתם מסקנה.");
    }
    
    if (hasRecommendation) {
      feedbacks.push("⭐ מעולה! הוספתם המלצה.");
    } else if (wordCount >= 10) {
      feedbacks.push("📝 חסרה המלצה! הוסיפו 'מומלץ ש...' או 'על כן, חשוב ש...'");
    }
    
    if (claim && !text.includes(claim?.substring(0, 15))) {
      feedbacks.push("💡 כדאי לחזור על הטענה שלכם (במילים אחרות) בסיכום.");
    }
  }
  
  else if (section === "refutation") {
    const hasRefutationStructure = /אמנם.*אולם|אמנם.*אך|למרות.*יש|נכון ש.*אך|אף על פי/.test(text);
    const mentionsOtherSide = /יש הטוענים|טוענים ש|יש האומרים|הצד השני|מצד שני/.test(text);
    
    if (isFragment) {
      feedbacks.push("⚠️ זה לא משפט שלם. הפרכה חייבת להיות לפחות משפט שלם.");
      feedbacks.push("💡 דוגמה: 'אמנם יש הטוענים שטלפונים עוזרים ללמידה, אולם מחקרים מראים שהם דווקא פוגעים בריכוז.'");
      return feedbacks.join("\n");
    }
    
    if (isPartialSentence) {
      feedbacks.push("⚠️ המשפט לא שלם ולא ברור. הפרכה צריכה משפט מלא עם מבנה 'אמנם... אולם...'.");
      return feedbacks.join("\n");
    }
    
    if (!endsWithPeriod && wordCount > 5) {
      feedbacks.push("⚠️ המשפט לא מסתיים בנקודה.");
    }
    
    // Content relevance
    const looksLikeRegularArgument = /ראשית|שנית|מפני ש/.test(text) && !mentionsOtherSide && !hasRefutationStructure;
    if (looksLikeRegularArgument) {
      feedbacks.push("⚠️ נראה שכתבתם נימוק רגיל ולא הפרכה! הפרכה מתייחסת לצד השני ומסבירה למה הוא לא צודק. השתמשו ב'אמנם... אולם...'.");
      return feedbacks.join("\n");
    }
    
    if (hasRefutationStructure) {
      feedbacks.push("🌟 מבנה הפרכה מצוין! השתמשתם ב'אמנם... אולם...' – בדיוק כמו שצריך!");
    } else if (mentionsOtherSide) {
      feedbacks.push("👍 טוב שהתייחסתם לצד השני! נסו להשתמש במבנה 'אמנם... אולם...' כדי לחזק את ההפרכה.");
    } else {
      feedbacks.push("⚠️ ההפרכה צריכה להתייחס לנימוק של הצד השני. נסו: 'אמנם יש הטוענים ש... אולם...'");
    }
    
    if (wordCount > 15) {
      feedbacks.push("📝 הפרכה מפותחת – כל הכבוד!");
    } else if (wordCount >= 8) {
      feedbacks.push("✏️ נסו להרחיב קצת – הסבירו למה הנימוק של הצד השני לא מספיק חזק.");
    }
  }
  
  else if (section === "full") {
    feedbacks.push("🎉 כתבתם טקסט טיעוני מלא – הישג מרשים!");
    
    const hasOpening = text.length > 50;
    const hasClaim = /לדעתי|אני סבור|עמדתי/.test(text);
    const hasRefutation = /אמנם.*אולם|למרות|אף על פי|נכון ש.*אך/.test(text);
    const hasSummary = /לסיכום|לאור|מכל הסיבות/.test(text);
    const hasConnectors = /ראשית|שנית|נוסף|לדוגמה|למשל/.test(text);
    
    if (hasClaim) feedbacks.push("✅ הטענה מופיעה בטקסט.");
    if (hasRefutation) feedbacks.push("✅ יש הפרכה – מעולה!");
    if (hasSummary) feedbacks.push("✅ יש פסקת סיכום.");
    if (hasConnectors) feedbacks.push("✅ שימוש במילות קישור.");
    
    const missing = [];
    if (!hasClaim) missing.push("טענה ברורה");
    if (!hasRefutation) missing.push("הפרכה עם 'אמנם... אולם...'");
    if (!hasSummary) missing.push("מילת סיכום");
    
    if (missing.length > 0) {
      feedbacks.push(`💡 שימו לב: כדאי לוודא שיש ${missing.join(", ")}.`);
    }
  }

  else if (section === "draft") {
    // content format: "נימוקים בעד:\n1. xxx\n2. yyy\n\nנימוקים נגד:\n1. xxx\n2. yyy"
    const prosMatch = text.match(/נימוקים בעד:\n([\s\S]*?)(?=\nנימוקים נגד:|$)/);
    const consMatch = text.match(/נימוקים נגד:\n([\s\S]*?)$/);
    const prosLines = prosMatch ? prosMatch[1].split("\n").filter(l => l.trim().length > 2) : [];
    const consLines = consMatch ? consMatch[1].split("\n").filter(l => l.trim().length > 2) : [];
    
    // === DUPLICATE / SIMILARITY DETECTION ===
    const normalize = (s) => s.replace(/^\d+\.\s*/, "").trim().replace(/[.,!?]/g, "").toLowerCase();
    const getWords = (s) => normalize(s).split(/\s+/).filter(w => w.length > 2);
    
    // Check similarity between two lines
    const areSimilar = (a, b) => {
      const na = normalize(a);
      const nb = normalize(b);
      // Exact or near-exact match
      if (na === nb) return true;
      // One contains the other
      if (na.includes(nb) || nb.includes(na)) return true;
      // Word overlap check
      const wa = getWords(a);
      const wb = getWords(b);
      if (wa.length === 0 || wb.length === 0) return false;
      const shared = wa.filter(w => wb.includes(w));
      const overlapRatio = shared.length / Math.min(wa.length, wb.length);
      return overlapRatio >= 0.6; // 60% word overlap = similar idea
    };
    
    // Find duplicates within pros
    const prosDuplicates = [];
    for (let i = 0; i < prosLines.length; i++) {
      for (let j = i + 1; j < prosLines.length; j++) {
        if (areSimilar(prosLines[i], prosLines[j])) prosDuplicates.push([i, j]);
      }
    }
    // Find duplicates within cons
    const consDuplicates = [];
    for (let i = 0; i < consLines.length; i++) {
      for (let j = i + 1; j < consLines.length; j++) {
        if (areSimilar(consLines[i], consLines[j])) consDuplicates.push([i, j]);
      }
    }
    // Find duplicates across pros and cons (same idea on both sides)
    const crossDuplicates = [];
    for (let i = 0; i < prosLines.length; i++) {
      for (let j = 0; j < consLines.length; j++) {
        if (areSimilar(prosLines[i], consLines[j])) crossDuplicates.push([i, j]);
      }
    }
    
    const hasDuplicates = prosDuplicates.length > 0 || consDuplicates.length > 0 || crossDuplicates.length > 0;
    
    if (hasDuplicates) {
      feedbacks.push("⚠️ שימו לב – יש רעיונות שחוזרים על עצמם!");
      if (prosDuplicates.length > 0) {
        const [i, j] = prosDuplicates[0];
        feedbacks.push(`🔄 בנימוקים בעד: "${normalize(prosLines[i])}" ו-"${normalize(prosLines[j])}" – זה אותו רעיון! נסו לחשוב על רעיון שונה.`);
      }
      if (consDuplicates.length > 0) {
        const [i, j] = consDuplicates[0];
        feedbacks.push(`🔄 בנימוקים נגד: "${normalize(consLines[i])}" ו-"${normalize(consLines[j])}" – זה אותו רעיון! נסו לחשוב על רעיון שונה.`);
      }
      if (crossDuplicates.length > 0) {
        const [i, j] = crossDuplicates[0];
        feedbacks.push(`🔄 כתבתם את אותו רעיון גם בעד וגם נגד: "${normalize(prosLines[i])}" ו-"${normalize(consLines[j])}". כל צד צריך רעיונות שונים!`);
      }
      feedbacks.push("💡 כל הכללה צריכה להיות רעיון **אחר** – זווית שונה על הנושא. חשבו: מה עוד קשור לנושא שלא כתבתם?");
    } else {
      feedbacks.push("👏 יופי שהקדשתם זמן לחשוב על רעיונות לשני הצדדים!");
    }
    
    if (prosLines.length >= 2) {
      feedbacks.push(`✅ כתבתם ${prosLines.length} רעיונות בעד.`);
    } else if (prosLines.length === 1) {
      feedbacks.push("📝 יש רעיון אחד בעד. חשבו על עוד אחד לפחות.");
    }
    
    if (consLines.length >= 2) {
      feedbacks.push(`✅ כתבתם ${consLines.length} רעיונות נגד.`);
    } else if (consLines.length === 1) {
      feedbacks.push("📝 יש רעיון אחד נגד. חשבו על עוד אחד לפחות.");
    }
    
    // Detect specific examples vs generalizations
    const specificPatterns = [
      /חבר שלי/i, /אח[ותי]? שלי/i, /אמא שלי/i, /אבא שלי/i, /המורה שלי/i, /הבת שלי/i, /הבן שלי/i,
      /פעם אחת/i, /יום אחד/i, /פעם ש/i, /כשהייתי/i, /קרה לי/i, /ראיתי ש/i, /שמעתי ש/i,
      /ילד אחד/i, /תלמיד אחד/i, /בן אדם אחד/i, /מישהו ש/i,
      /בבית ספר שלנו/i, /בכיתה שלנו/i, /אצלנו/i,
      /למשל אני/i, /אני תמיד/i, /אני אף פעם/i,
      /מצלמ/i, /מעתיק/i, /משחק/i, /יושב על/i, /גולש ב/i, /צופ[הה] ב/i,
      /סיפור/i, /מקרה/i, /אירוע/i,
    ];
    
    const allLines = [...prosLines, ...consLines];
    const specificLines = allLines.filter(line => specificPatterns.some(p => p.test(line)));
    
    if (specificLines.length > 0) {
      feedbacks.push(`⚠️ ${specificLines.length > 1 ? "חלק מהרעיונות נראים" : "אחד הרעיונות נראה"} כמו דוגמה ספציפית ולא כמו הכללה!`);
      feedbacks.push("🔑 בטיוטה כותבים **הכללות** – רעיונות כלליים, לא מקרים פרטיים.");
      const firstSpecific = specificLines[0].replace(/^\d+\.\s*/, "").trim();
      feedbacks.push(`💡 למשל: במקום "${firstSpecific}" → חשבו מה התופעה הכללית? (פגיעה בריכוז? שימוש לרעה? חוסר פרטיות?)`);
    } else if (allLines.length >= 2 && !hasDuplicates) {
      feedbacks.push("🌟 כתבתם הכללות ולא דוגמאות ספציפיות – בדיוק כמו שצריך!");
    }
    
    // === PER-ITEM CONTENT QUALITY ===
    const vagueSingleWords = ["טלפונים", "טכנולוגיה", "ריכוז", "בריאות", "למידה", "חינוך", "בטיחות", "חופש", "כסף", "זמן", "חברים", "הורים", "מורים", "ילדים", "מידע", "משחקים", "אלימות", "סכנה"];
    
    const analyzeItem = (line, label) => {
      const clean = line.replace(/^\d+\.\s*/, "").trim();
      const words = clean.split(/\s+/).filter(w => w.length > 0);
      
      // Too short - 1 word
      if (words.length === 1) {
        if (vagueSingleWords.includes(clean)) {
          feedbacks.push(`⚠️ ${label}: "${clean}" – מילה אחת זה לא מספיק ולא ברור. מה לגבי ${clean}? נסו: "פגיעה ב${clean}" או "השפעה על ה${clean}".`);
        } else {
          feedbacks.push(`⚠️ ${label}: "${clean}" – קצר מדי. פרטו: מה בדיוק הרעיון?`);
        }
        return "short";
      }
      
      // 2 words - might be ok but check
      if (words.length === 2) {
        feedbacks.push(`💡 ${label}: "${clean}" – קצר. נסו להרחיב קצת, למשל: "פגיעה בריכוז בזמן שיעור" או "בריונות רשת בקרב בני נוער".`);
        return "short";
      }
      
      // Check vague/unclear
      const vaguePatterns = /^(דברים|משהו|בעיה|עניין|נושא|דבר)\s/i;
      if (vaguePatterns.test(clean)) {
        feedbacks.push(`⚠️ ${label}: "${clean}" – לא ברור מספיק. מה בדיוק הדבר? נסחו כתופעה ספציפית.`);
        return "vague";
      }
      
      // Good generalization patterns
      const goodPatterns = /פגיעה ב|השפעה על|שימוש ב|שימוש ל|חשיפה ל|צמצום|הגברת|הגבלת|שיפור|עידוד|הרחבת|העלאת|הורדת|מניעת|קידום|פיתוח|חיזוק|היחלשות|עלייה ב|ירידה ב/;
      if (goodPatterns.test(clean) && words.length >= 3) {
        return "good";
      }
      
      // Moderate - has content but could be better
      if (words.length >= 3) {
        return "ok";
      }
      
      return "ok";
    };
    
    let goodCount = 0;
    let problemCount = 0;
    
    prosLines.forEach((line, i) => {
      const result = analyzeItem(line, `בעד ${i + 1}`);
      if (result === "good") goodCount++;
      if (result === "short" || result === "vague") problemCount++;
    });
    consLines.forEach((line, i) => {
      const result = analyzeItem(line, `נגד ${i + 1}`);
      if (result === "good") goodCount++;
      if (result === "short" || result === "vague") problemCount++;
    });
    
    if (goodCount > 0 && problemCount === 0 && specificLines.length === 0 && !hasDuplicates) {
      feedbacks.push("🌟 מעולה! הכללות ברורות, מנוסחות היטב ומגוונות. הדוגמאות הספציפיות יבואו בשלב הנימוקים!");
    } else if (goodCount > 0) {
      feedbacks.push(`✨ ${goodCount === 1 ? "רעיון אחד מנוסח" : goodCount + " רעיונות מנוסחים"} יפה כהכללה!`);
    }
  }
  
  return feedbacks.join("\n");
}

// === UTILITY: Detect incomplete/trailing sentences ===
function checkSentenceCompleteness(text) {
  if (!text || text.trim().length < 10) return [];
  const warnings = [];
  
  // Patterns that indicate a sentence was cut mid-thought
  const trailingEndings = [
    { pattern: /\sגם\s*[.!?]?\s*$/, word: "גם" },
    { pattern: /\sש\s*[.!?]?\s*$/, word: "ש" },
    { pattern: /\sכי\s*[.!?]?\s*$/, word: "כי" },
    { pattern: /\sאבל\s*[.!?]?\s*$/, word: "אבל" },
    { pattern: /\sמפני ש\s*[.!?]?\s*$/, word: "מפני ש" },
    { pattern: /\sבגלל ש?\s*[.!?]?\s*$/, word: "בגלל" },
    { pattern: /\sכמו\s*[.!?]?\s*$/, word: "כמו" },
    { pattern: /\sכמו כן\s*[.!?]?\s*$/, word: "כמו כן" },
    { pattern: /\sעל ידי\s*[.!?]?\s*$/, word: "על ידי" },
    { pattern: /\sכדי ש?\s*[.!?]?\s*$/, word: "כדי" },
    { pattern: /\sבזכות\s*[.!?]?\s*$/, word: "בזכות" },
    { pattern: /\sבשל\s*[.!?]?\s*$/, word: "בשל" },
    { pattern: /\sלמרות ש?\s*[.!?]?\s*$/, word: "למרות" },
    { pattern: /\sאף על פי ש\s*[.!?]?\s*$/, word: "אף על פי ש" },
    { pattern: /\sכגון\s*[.!?]?\s*$/, word: "כגון" },
    { pattern: /\sכפי ש\s*[.!?]?\s*$/, word: "כפי ש" },
    { pattern: /\sלפי\s*[.!?]?\s*$/, word: "לפי" },
    { pattern: /\sעקב\s*[.!?]?\s*$/, word: "עקב" },
    { pattern: /\sמשום ש\s*[.!?]?\s*$/, word: "משום ש" },
    { pattern: /\sבנוסף\s*[.!?]?\s*$/, word: "בנוסף" },
    { pattern: /\sוגם\s*[.!?]?\s*$/, word: "וגם" },
    { pattern: /\sאלא\s*[.!?]?\s*$/, word: "אלא" },
    { pattern: /\sאולם\s*[.!?]?\s*$/, word: "אולם" },
    { pattern: /\sלכן\s*[.!?]?\s*$/, word: "לכן" },
    { pattern: /\sאם\s*[.!?]?\s*$/, word: "אם" },
    { pattern: /\sכאשר\s*[.!?]?\s*$/, word: "כאשר" },
    { pattern: /\sאשר\s*[.!?]?\s*$/, word: "אשר" },
  ];
  
  // Split into sentences, check each one
  const parts = text.split(/(?<=[.!?])\s*/);
  // Also check the last segment (may not have punctuation)
  const allParts = [...parts];
  
  for (const part of allParts) {
    const trimmed = part.trim();
    if (trimmed.length < 8) continue;
    
    for (const { pattern, word } of trailingEndings) {
      if (pattern.test(trimmed)) {
        const shortText = trimmed.length > 50 ? "..." + trimmed.slice(-50) : trimmed;
        warnings.push(`⚠️ המשפט "${shortText}" נקטע באמצע! מה רציתם לומר אחרי "${word}"? השלימו את המשפט.`);
        break;
      }
    }
  }
  
  // Check for sentence without ending punctuation (not fragment)
  const trimmedText = text.trim();
  const wordCount = trimmedText.split(/\s+/).length;
  if (wordCount >= 6 && !/[.!?]$/.test(trimmedText)) {
    warnings.push("⚠️ המשפט לא מסתיים בנקודה, סימן שאלה או סימן קריאה. כל משפט חייב להסתיים בסימן פיסוק.");
  }
  
  return warnings;
}

async function getAIFeedback(section, content, topic, claim, side) {
  const text = (content || "").trim();
  const wordCount = text.split(/\s+/).filter(w => w.length > 0).length;

  // === ALWAYS check sentence completeness first (local, fast) ===
  const sentenceWarnings = section !== "draft" ? checkSentenceCompleteness(text) : [];

  // === ALWAYS run basic quality checks first ===
  if (!text || wordCount < 3) {
    return "✏️ נראה שעדיין לא כתבתם מספיק. נסו לכתוב לפחות משפט שלם אחד כדי שאוכל לתת משוב!";
  }

  const isGibberish = /^[אבגדהוזחטיכלמנסעפצקרשת\s]{1,10}$/.test(text) || 
    /בלה\s*בלה/i.test(text) || /אאא|בבב|גגג/.test(text);
  if (isGibberish) {
    return "🤔 נראה שהטקסט עדיין לא מוכן לבדיקה. נסו לכתוב תוכן אמיתי ואז אבדוק שוב!";
  }

  const endsWithPeriod = /[.!?]$/.test(text.trim());
  const isFragment = wordCount < 6 && !endsWithPeriod;
  const isPartialSentence = wordCount >= 3 && wordCount < 8 && !endsWithPeriod;

  // For fragment/partial sentences - return rule-based feedback immediately, DON'T call AI
  if (section !== "draft" && (isFragment || isPartialSentence)) {
    return getRuleBasedFeedback(section, content, topic, claim, side);
  }

  // For short content that lacks depth - also use rule-based (AI will be too lenient)
  if (section === "arguments" && wordCount < 15) {
    return getRuleBasedFeedback(section, content, topic, claim, side);
  }
  if (section === "summary" && wordCount < 12) {
    return getRuleBasedFeedback(section, content, topic, claim, side);
  }
  if (section === "refutation" && wordCount < 10) {
    return getRuleBasedFeedback(section, content, topic, claim, side);
  }
  if (section === "opening" && wordCount < 15) {
    return getRuleBasedFeedback(section, content, topic, claim, side);
  }
  if (section === "claim" && wordCount < 5) {
    return getRuleBasedFeedback(section, content, topic, claim, side);
  }

  // Also use rule-based if text doesn't end with punctuation (likely incomplete)
  if (section !== "draft" && !endsWithPeriod && wordCount < 20) {
    return getRuleBasedFeedback(section, content, topic, claim, side);
  }

  const sectionInstructions = {
    opening: `בדוק את פסקת הפתיחה של התלמיד/ה. הפתיחה צריכה:
- להציג את הנושא באופן כללי
- להציג דילמה, התלבטות או שאלה סביב הנושא – חייב להיות ברור שיש ויכוח/מחלוקת
- לעורר עניין אצל הקורא
- לא לחשוף את דעת הכותב

בדוק במיוחד (חשוב!):
1. האם יש דילמה/התלבטות/שאלה? הפתיחה חייבת להראות שיש שני צדדים לנושא.
   דרכים טובות: שאלה רטורית ("האם...?"), הצגת שני צדדים ("יש הטוענים... ויש..."), ציון שהנושא שנוי במחלוקת.
   אם הפתיחה רק מציגה את הנושא בלי להראות שיש ויכוח – ציין! ותן דוגמה איך להוסיף דילמה.
   למשל: אם כתב "בימינו יש טלפונים ניידים" – זה לא מספיק. צריך: "בימינו יש טלפונים ניידים, ועולה השאלה האם מותר להשתמש בהם בבתי ספר".

2. האם הפתיחה חושפת דעה? 
   חשוב מאוד: הבדל בין חשיפת דעה להצגת דילמה!
   
   ❌ חשיפת דעה (בעייתי): "לדעתי צריך לאסור", "אני חושב ש...", "ברור שצריך", "נראה לי ש..."
   ✅ הצגת דילמה (מצוין!): "נשאלת השאלה האם צריכים לאסור... או לא", "האם יש לאפשר... או להגביל?"
   
   כלל ברזל: מילים כמו "צריך", "לאסור", "חייבים", "לאפשר" שמופיעות בתוך שאלה או דילמה ("האם...", "נשאלת השאלה", "עולה השאלה", "...או לא") – זו לא חשיפת דעה! זו הצגה מצוינת של הדילמה.
   
   רק ביטויים שמביעים עמדה אישית ישירה הם בעייתיים: "לדעתי", "אני חושב", "נראה לי", "בעיניי", "ברור לי", "בהחלט כן/לא".
   
3. האם הפתיחה ברורה ומנוסחת היטב?

4. סימני פיסוק ומשלב לשוני:
   - האם יש נקודה בסוף המשפטים?
   - האם הניסוח ברמה תקנית (לא דיבורי)?

אם היא קצרה מדי או לא ברורה – ציין.
שים לב: אל תדרוש סגנון מסוים – קבל כל סגנון פתיחה (שאלה, ציטוט, נתון, סיפור, כללי), אבל חייבת להיות דילמה/שאלה.`,
    claim: `בדוק את הטענה של התלמיד/ה. הטענה צריכה:
- להיות ברורה וחד-משמעית
- להביע עמדה ברורה (בעד או נגד)
- להיות ניתנת לביסוס
העמדה שנבחרה: ${side === "pro" ? "בעד" : "נגד"}.
אם הטענה מהססת או לא ברורה – ציין. אם היא טובה – שבח.`,
    arguments: `בדוק את הנימוקים והדוגמאות של התלמיד/ה.

בתחתית הטקסט מופיעות "הכללות מהטיוטה" – אלו הרעיונות הכלליים שהתלמיד/ה רשם/ה קודם. השתמש בהם כדי לבדוק קישוריות.

בדוק כל נימוק לפי הקריטריונים הבאים:

1. קישוריות להכללה מהטיוטה:
   - האם הנימוק מפתח את ההכללה המתאימה שנרשמה בטיוטה?
   - אם הנימוק סוטה מההכללה – ציין: "ההכללה שלך הייתה X, אבל הנימוק מדבר על Y"
   - אם הנימוק מתאים – ציין: "הנימוק מפתח יפה את ההכללה"

2. קישוריות בין נימוק לדוגמה:
   - האם הדוגמה/ההסבר באמת תומכ/ת בנימוק?
   - האם הקשר ברור? אם לא – ציין: "מה הקשר בין הדוגמה לנימוק?"

3. בהירות הרעיון:
   - האם הנימוק ברור? האם הקורא יבין מה רציתם להגיד?
   - אם לא ברור – הסבר מה חסר ותן דוגמה לניסוח טוב יותר

4. סימני פיסוק:
   - האם יש נקודה בסוף כל משפט?
   - האם יש פסיקים במקומות הנכונים (אחרי מילות קישור, בין פסוקיות)?
   - אם חסרים – ציין בדיוק היכן

5. משלב לשוני:
   - האם הניסוח ברמה תקנית/ספרותית ולא דיבורית?
   - ביטויים דיבוריים כמו "סבבה", "יאללה", "פשוט", "ממש", "וואלה", "בקטנה", "נורא" (=מאוד) – לא מתאימים
   - אם יש ניסוח דיבורי – ציין והצע חלופה תקנית

6. תמיכה בטענה:
   - האם הנימוק תומך בטענה "${claim || ""}"?

תן משוב פר-נימוק. שבח נימוקים טובים, אל תשבח חלשים/לא קשורים/לא ברורים!`,
    summary: `בדוק את פסקת הסיכום. הסיכום צריך:
- לחזור על הטענה (במילים אחרות)
- להסיק מסקנה
- להמליץ או לקרוא לפעולה
אם הסיכום מוסיף נימוקים חדשים – ציין שלא מומלץ. אם הוא מוצלח – שבח.`,
    refutation: `בדוק את ההפרכה. הפרכה טובה צריכה:
- להתייחס לנימוק של הצד השני
- להסביר למה הנימוק הזה לא מספיק חזק
- להשתמש במבנה "אמנם... אולם..." או דומה
אם ההפרכה לא מתייחסת לצד השני – ציין. אם היא מוצלחת – שבח.`,
    full: `בדוק את הטקסט הטיעוני המלא עם הפרכה. בדוק:
- האם הפתיחה כללית ולא חושפת דעה?
- האם הטענה ברורה?
- האם הנימוקים תומכים בטענה ומלווים בדוגמאות?
- האם יש הפרכה שמתייחסת לצד השני?
- האם הסיכום חוזר על הטענה ומסיק מסקנה?
- האם יש שימוש במילות קישור?
תן משוב כללי על הטקסט כולו.`,
    draft: `בדוק את הרעיונות שהתלמיד/ה רשם/ה בשלב הטיוטה – בעד ונגד.
הנושא: "${topic || ""}"

בדוק כל רעיון לפי הקריטריונים הבאים (בסדר הזה):

1. כפילויות רעיוניות (קודם כל!):
   - האם יש רעיונות שחוזרים על עצמם? גם אם המילים שונות, אם הרעיון המרכזי זהה – ציין!
   - למשל: "פגיעה בריכוז" ו-"הפרעה לריכוז" = אותו רעיון!
   - אם מצאת כפילות – ציין בדיוק אילו רעיונות דומים ובקש לחשוב על רעיון אחר

2. הכללה מול דוגמה ספציפית:
   - בטיוטה צריך **הכללות** (תופעות כלליות) ולא דוגמאות ספציפיות
   - הכללה = "פגיעה בריכוז", "בריונות רשת", "שימוש לרעה בטכנולוגיה"
   - דוגמה ספציפית = "ילדים מצלמים מורים", "חבר שלי על הטיקטוק"
   - אם מצאת דוגמה ספציפית – הצע מה ההכללה שעומדת מאחוריה

3. עומק ובהירות התוכן (חשוב!):
   לכל רעיון בנפרד, בדוק:
   - האם הרעיון ברור ומובן? או שהוא מעורפל/לא ברור?
   - האם הניסוח מדויק? למשל: "טלפונים" לבד = לא ברור. "פגיעה בריכוז עקב שימוש בטלפונים" = ברור.
   - האם הרעיון מספיק מפורט? מילה אחת או שתיים זה לא מספיק – צריך ביטוי שלם שמתאר תופעה.
   - האם ההכללה מנוסחת היטב? ביטוי כמו "דברים רעים" = לא מנוסח. "פגיעה באינטראקציה חברתית" = מנוסח היטב.
   - אם הרעיון חלש/מעורפל/קצר מדי – ציין לגבי אותו רעיון ספציפית ותן דוגמה לניסוח טוב יותר.

4. רלוונטיות לנושא:
   - האם כל רעיון באמת קשור לנושא?
   - אם לא – ציין ושאל למה הוא חושב שזה קשור

5. מגוון:
   - האם הרעיונות מייצגים זוויות שונות (חברתי, לימודי, בריאותי, רגשי...)?

תן משוב פר-רעיון: עבור על כל רעיון ותן לו הערה קצרה (טוב/לשפר/לא ברור).
שבח רעיונות טובים, אבל אל תשבח רעיונות חלשים, מעורפלים, כפולים או ספציפיים מדי!`,
  };

  // Try AI feedback first
  try {
    const response = await fetch("https://api.anthropic.com/v1/messages", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({
        model: "claude-sonnet-4-20250514",
        max_tokens: 1000,
        system: `אתה מורה לכתיבה טיעונית בחטיבת ביניים בישראל. תפקידך לתת משוב חינוכי, מעודד ובונה לתלמידים.

כללי משוב חשובים מאוד – בדוק בסדר הזה:

1. תקינות המשפטים (קודם כל! זה הכי חשוב!):
   בדוק כל משפט בנפרד:
   
   א. שלמות המשפט:
   - האם המשפט מסתיים? משפט שנקטע באמצע ("עם הפריצה הגדולה של הבינה המלאכותית ניתן לראות גם") = משפט לא שלם!
   - סימנים למשפט קטוע: מסתיים ב"גם", "ש", "כי", "אבל", "מפני ש", "בגלל", "כמו", "על ידי" – חסרה ההשלמה!
   - סימנים נוספים: מתחיל ב"עם..." או "בגלל ש..." אבל לא מגיע למסקנה/תוצאה
   - אם משפט נקטע – ציין: "⚠️ המשפט נקטע באמצע! מה רציתם לומר אחרי '...'?" ותן דוגמה להשלמה
   
   ב. מבנה תחבירי:
   - האם יש נושא + נשוא (פועל) + השלמה?
   - אם חסר פועל, או חסר נושא – ציין ותן דוגמה
   - אל תשבח טקסט שהוא חלק ממשפט!
   
   ג. סימני פיסוק:
   - האם המשפט מסתיים בנקודה/סימן שאלה/סימן קריאה?
   - האם יש פסיקים אחרי מילות קישור (ראשית, שנית, לדעתי, בנוסף) ובין פסוקיות?
   - אם חסר סימן פיסוק – ציין בדיוק היכן
   
   ד. משלב לשוני:
   - האם הניסוח תקני/ספרותי ולא דיבורי?
   - ביטויים דיבוריים: "סבבה", "יאללה", "פשוט", "ממש", "וואלה", "בקטנה", "נורא" (=מאוד), "חרא", "אחלה"
   - אם יש ניסוח דיבורי – ציין והצע חלופה תקנית

2. התאמה לשלב הנדרש:
   - האם מה שנכתב מתאים לסוג הכתיבה שהתבקש? (פתיחה? טענה? נימוק? סיכום? הפרכה?)
   - פתיחה – צריכה להיות ניטרלית, להציג נושא ודילמה, לא לחשוף דעה אישית
     חשוב: מילות דעה ("צריך", "לאסור", "לאפשר") בתוך שאלה/דילמה ("האם צריך?", "נשאלת השאלה האם... או לא") = הצגת דילמה, לא חשיפת דעה!
   - טענה – צריכה להביע עמדה ברורה ונחרצת
   - נימוק – צריך להיות סיבה שתומכת בטענה, עם דוגמה
   - סיכום – חזרה על הטענה, מסקנה, המלצה
   - הפרכה – התייחסות לצד השני עם "אמנם... אולם..."
   - אם התלמיד כתב טענה במקום פתיחה, או פתיחה במקום טענה – ציין!

3. איכות התוכן:
   - האם הטקסט רלוונטי לנושא "${topic || ""}"?
   - האם הטקסט ברור ומובן?
   - האם יש עומק מספיק?
   - האם יש סימני פיסוק תקינים?
   - האם המשלב הלשוני תקני (לא דיבורי)?

כללי ניסוח המשוב:
- היה ספציפי: במקום "יפה" כתוב מה בדיוק טוב ומה לתקן
- תן דוגמה מתוקנת כשמשהו לא תקין
- הגבל ל-4-6 משפטים
- השתמש באימוג'י
- שפה פשוטה לבני נוער

הנושא: "${topic || ""}"`,
        messages: [
          {
            role: "user",
            content: `${sectionInstructions[section] || ""}\n\nתוכן התלמיד/ה:\n"${content}"`,
          },
        ],
      }),
    });

    if (!response.ok) {
      console.warn("AI feedback HTTP error:", response.status);
      return getRuleBasedFeedback(section, content, topic, claim, side);
    }

    const result = await response.json();

    if (result.error) {
      console.warn("AI feedback API error:", result.error);
      return getRuleBasedFeedback(section, content, topic, claim, side);
    }

    const text = result.content
      ?.filter(c => c.type === "text")
      ?.map(c => c.text)
      ?.join("\n") || "";

    if (!text.trim()) {
      const ruleFb = getRuleBasedFeedback(section, content, topic, claim, side);
      return sentenceWarnings.length > 0 ? sentenceWarnings.join("\n") + "\n\n" + ruleFb : ruleFb;
    }

    return sentenceWarnings.length > 0 ? sentenceWarnings.join("\n") + "\n\n" + text : text;
  } catch (e) {
    console.warn("AI feedback network error:", e);
    // Fallback to rule-based feedback
    const ruleFb = getRuleBasedFeedback(section, content, topic, claim, side);
    return sentenceWarnings.length > 0 ? sentenceWarnings.join("\n") + "\n\n" + ruleFb : ruleFb;
  }
}

// ==================== UI COMPONENTS ====================

function ProgressBar({ currentStep, totalSteps, stepNames, onStepClick }) {
  return (
    <div style={{ padding: "16px 0", marginBottom: 20 }}>
      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", position: "relative" }}>
        <div style={{
          position: "absolute", top: "50%", right: 20, left: 20, height: 3,
          background: "#e0d6f0", transform: "translateY(-50%)", zIndex: 0, borderRadius: 2,
        }} />
        <div style={{
          position: "absolute", top: "50%", right: 20, height: 3,
          background: "linear-gradient(to left, #6a4fa0, #9a75d6)",
          transform: "translateY(-50%)", zIndex: 1, borderRadius: 2,
          width: `${((currentStep) / (totalSteps - 1)) * (100 - 6)}%`,
          transition: "width 0.6s cubic-bezier(0.4, 0, 0.2, 1)",
        }} />
        {stepNames.map((name, i) => (
          <div key={i} style={{ display: "flex", flexDirection: "column", alignItems: "center", zIndex: 2, flex: 1, cursor: onStepClick ? "pointer" : "default" }}
            onClick={() => onStepClick && onStepClick(i)}
            title={onStepClick ? `לחצו כדי לעבור ל: ${name}` : ""}>
            <div style={{
              width: i <= currentStep ? 34 : 26, height: i <= currentStep ? 34 : 26,
              borderRadius: "50%", display: "flex", alignItems: "center", justifyContent: "center",
              background: i < currentStep ? "linear-gradient(135deg, #6a4fa0, #9a75d6)"
                : i === currentStep ? "linear-gradient(135deg, #e8853a, #f7c040)" : "#e8e0f0",
              color: i <= currentStep ? "#fff" : "#9a8cb8",
              fontWeight: 800, fontSize: i <= currentStep ? 14 : 12,
              boxShadow: i === currentStep ? "0 0 0 3px rgba(232,133,58,0.25)" : "none",
              transition: "all 0.4s ease",
            }}>
              {i < currentStep ? "✓" : i + 1}
            </div>
            <span style={{
              fontSize: 10, marginTop: 5, color: i <= currentStep ? "#5a3e8e" : "#b0a4c4",
              fontWeight: i === currentStep ? 700 : 500, textAlign: "center",
              maxWidth: 70, lineHeight: 1.2,
              textDecoration: onStepClick ? "none" : "none",
            }}>{name}</span>
          </div>
        ))}
      </div>
    </div>
  );
}

function StageCard({ title, icon, children, color = "#6a4fa0" }) {
  return (
    <div style={{
      background: "#fff", borderRadius: 20, padding: "30px 32px",
      boxShadow: "0 4px 24px rgba(90,62,142,0.07)",
      borderTop: `4px solid ${color}`, marginBottom: 22,
      animation: "fadeSlideIn 0.5s ease-out",
    }}>
      <h2 style={{ fontSize: 26, color, margin: "0 0 22px", display: "flex", alignItems: "center", gap: 10, fontFamily: "'Heebo', sans-serif" }}>
        <span style={{ fontSize: 32 }}>{icon}</span> {title}
      </h2>
      {children}
    </div>
  );
}

function TextArea({ value, onChange, placeholder, rows = 3, label, helperText }) {
  return (
    <div style={{ marginBottom: 16 }}>
      {label && <label style={{ display: "block", fontWeight: 600, fontSize: 18, color: "#5a3e8e", marginBottom: 6 }}>{label}</label>}
      {helperText && <p style={{ fontSize: 16, color: "#8a7aaa", margin: "0 0 8px", lineHeight: 1.7 }}>{helperText}</p>}
      <textarea value={value} onChange={e => onChange(e.target.value)} placeholder={placeholder} rows={rows}
        style={{
          width: "100%", padding: "16px 18px", borderRadius: 12, border: "2px solid #e0d6f0",
          fontSize: 20, fontFamily: "'Heebo', sans-serif", resize: "vertical",
          outline: "none", transition: "border-color 0.3s", lineHeight: 1.9,
          direction: "rtl", boxSizing: "border-box", background: "#faf8ff",
        }}
        onFocus={e => e.target.style.borderColor = "#9a75d6"}
        onBlur={e => e.target.style.borderColor = "#e0d6f0"}
      />
    </div>
  );
}

function Button({ onClick, children, variant = "primary", disabled = false, style: s = {} }) {
  const styles = {
    primary: { background: "linear-gradient(135deg, #6a4fa0, #9070c0)", color: "#fff", boxShadow: "0 3px 12px rgba(106,79,160,0.25)" },
    secondary: { background: "linear-gradient(135deg, #e8853a, #f7c040)", color: "#5a3e0e", boxShadow: "0 3px 12px rgba(232,133,58,0.2)" },
    outline: { background: "transparent", color: "#6a4fa0", border: "2px solid #d0c4e8" },
    success: { background: "linear-gradient(135deg, #43a047, #66bb6a)", color: "#fff", boxShadow: "0 3px 12px rgba(67,160,71,0.25)" },
    feedback: { background: "linear-gradient(135deg, #0288d1, #29b6f6)", color: "#fff", boxShadow: "0 3px 12px rgba(2,136,209,0.25)" },
  };
  return (
    <button onClick={onClick} disabled={disabled}
      style={{
        padding: "16px 32px", borderRadius: 14, border: "none", fontSize: 18,
        fontWeight: 700, cursor: disabled ? "not-allowed" : "pointer",
        fontFamily: "'Heebo', sans-serif", transition: "all 0.3s",
        opacity: disabled ? 0.5 : 1, ...styles[variant], ...s,
      }}
      onMouseEnter={e => { if (!disabled) e.target.style.transform = "translateY(-1px)"; }}
      onMouseLeave={e => { e.target.style.transform = "translateY(0)"; }}
    >{children}</button>
  );
}

function ConnectorChips({ type, onSelect }) {
  return (
    <div style={{ display: "flex", flexWrap: "wrap", gap: 10, marginBottom: 14 }}>
      <span style={{ fontSize: 16, color: "#8a7aaa", alignSelf: "center", fontWeight: 600 }}>מילות קישור:</span>
      {CONNECTOR_WORDS[type]?.map((word, i) => (
        <button key={i} onClick={() => onSelect(word)}
          style={{
            padding: "8px 18px", borderRadius: 20, border: "1px solid #d0c4e8",
            background: "#f5f0ff", color: "#6b4fa0", fontSize: 16, cursor: "pointer",
            fontFamily: "'Heebo', sans-serif", transition: "all 0.2s",
          }}
          onMouseEnter={e => { e.target.style.background = "#e8dff5"; }}
          onMouseLeave={e => { e.target.style.background = "#f5f0ff"; }}
        >{word}</button>
      ))}
    </div>
  );
}

function InfoBox({ children, type = "info" }) {
  const c = {
    info: { bg: "#f0ecff", border: "#c4b5e3", icon: "💡", color: "#5a3e8e" },
    tip: { bg: "#fff8e8", border: "#f0d080", icon: "⭐", color: "#8a6a10" },
    warning: { bg: "#fff0f0", border: "#e8a0a0", icon: "⚠️", color: "#8a3030" },
    success: { bg: "#f0fff0", border: "#a0d8a0", icon: "✅", color: "#2a6a2a" },
  }[type];
  return (
    <div style={{
      background: c.bg, border: `1px solid ${c.border}`, borderRadius: 14,
      padding: "16px 20px", marginBottom: 18, display: "flex", gap: 12, alignItems: "flex-start",
    }}>
      <span style={{ fontSize: 22 }}>{c.icon}</span>
      <div style={{ fontSize: 18, color: c.color, lineHeight: 1.9 }}>{children}</div>
    </div>
  );
}

function FeedbackBox({ feedback, loading, onRetry }) {
  if (loading) return (
    <div style={{
      background: "linear-gradient(135deg, #e3f2fd, #f0f8ff)", border: "1px solid #90caf9",
      borderRadius: 14, padding: "16px 20px", marginTop: 14, textAlign: "center",
    }}>
      <div style={{ fontSize: 24, marginBottom: 6, animation: "pulse 1.5s infinite" }}>🔍</div>
      <p style={{ color: "#1565c0", fontSize: 14, margin: 0 }}>בודק את הכתיבה שלכם...</p>
    </div>
  );
  if (!feedback) return null;
  const isError = feedback.startsWith("⚠️");
  return (
    <div style={{
      background: isError ? "linear-gradient(135deg, #fff8e1, #fff3e0)" : "linear-gradient(135deg, #e3f2fd, #f0f8ff)",
      border: `1px solid ${isError ? "#ffcc02" : "#90caf9"}`,
      borderRadius: 14, padding: "16px 20px", marginTop: 14,
      animation: "fadeSlideIn 0.4s ease-out",
    }}>
      <h4 style={{ fontSize: 19, color: isError ? "#e65100" : "#0d47a1", margin: "0 0 10px", display: "flex", alignItems: "center", gap: 8 }}>
        {isError ? "⚠️ שגיאה" : "📝 משוב על הכתיבה שלכם:"}
      </h4>
      <p style={{ fontSize: 18, color: isError ? "#bf360c" : "#1a3a5c", lineHeight: 2.0, margin: 0, whiteSpace: "pre-wrap" }}>{feedback}</p>
      {isError && onRetry && (
        <button onClick={onRetry} style={{
          marginTop: 10, padding: "8px 20px", borderRadius: 10, border: "1px solid #e65100",
          background: "#fff3e0", color: "#e65100", fontSize: 14, cursor: "pointer",
          fontFamily: "'Heebo', sans-serif", fontWeight: 600,
        }}>🔄 נסו שוב</button>
      )}
    </div>
  );
}

function BackToTopicBanner({ topicTitle, sectionName }) {
  return (
    <div style={{
      background: "linear-gradient(135deg, #e8f5e9, #f1faf3)", borderRadius: 16,
      padding: "18px 22px", marginBottom: 20, border: "2px solid #a5d6a7",
      animation: "fadeSlideIn 0.5s ease-out",
    }}>
      <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 8 }}>
        <span style={{ fontSize: 24 }}>✅</span>
        <strong style={{ fontSize: 16, color: "#2e7d32" }}>סיימתם את התרגול! כל הכבוד! 🎉</strong>
      </div>
      <div style={{
        background: "#fff", borderRadius: 12, padding: "14px 18px",
        border: "1px solid #c8e6c9",
      }}>
        <p style={{ fontSize: 14, color: "#2a5a3a", margin: 0, lineHeight: 1.7 }}>
          <span style={{ fontSize: 18, marginLeft: 6 }}>📝</span>
          עכשיו <strong>נחזור לכתיבה שלכם</strong> בנושא:
        </p>
        <p style={{ fontSize: 17, fontWeight: 800, color: "#1b5e20", margin: "8px 0 0" }}>
          "{topicTitle}"
        </p>
        <p style={{ fontSize: 16, color: "#558b2f", margin: "6px 0 0" }}>
          ⬇️ כתבו את ה{sectionName} שלכם למטה
        </p>
      </div>
    </div>
  );
}

// ==================== QUIZ COMPONENTS ====================

function QuizOpenings({ onComplete }) {
  const [current, setCurrent] = useState(0);
  const [answered, setAnswered] = useState({});
  const [score, setScore] = useState(0);
  const shuffled = useRef([...OPENING_QUIZ].sort(() => Math.random() - 0.5).slice(0, 4));
  const q = shuffled.current[current];
  const total = shuffled.current.length;

  const answer = (userSaidGood) => {
    const correct = userSaidGood === q.isGood;
    setAnswered({ choice: userSaidGood, correct, explanation: q.explanation });
    if (correct) setScore(s => s + 1);
  };
  const next = () => {
    setAnswered({});
    if (current + 1 >= total) { onComplete(score + (answered.correct ? 0 : 0)); return; }
    setCurrent(c => c + 1);
  };

  return (
    <div style={{ background: "#f8f5ff", borderRadius: 16, padding: "20px 24px", marginBottom: 20, border: "1px solid #d8d0e8" }}>
      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 14 }}>
        <h3 style={{ fontSize: 18, color: "#5a3e8e", margin: 0 }}>🎮 תרגול: האם זו פתיחה טובה?</h3>
        <span style={{ fontSize: 16, color: "#8a7aaa" }}>{current + 1}/{total}</span>
      </div>
      <div style={{
        background: "#fff", borderRadius: 12, padding: "16px 20px", marginBottom: 14,
        border: "1px solid #e8e0f0", fontSize: 20, lineHeight: 1.9, color: "#2a1a4a",
      }}>
        "{q.text}"
      </div>
      {!answered.choice && answered.choice !== false ? (
        <div style={{ display: "flex", gap: 12 }}>
          <button onClick={() => answer(true)} style={{
            flex: 1, padding: "14px", borderRadius: 12, border: "2px solid #a5d6a7", background: "#f1f8f1",
            fontSize: 18, fontWeight: 700, cursor: "pointer", fontFamily: "'Heebo', sans-serif", color: "#2e7d32",
          }}>✅ פתיחה טובה</button>
          <button onClick={() => answer(false)} style={{
            flex: 1, padding: "14px", borderRadius: 12, border: "2px solid #ef9a9a", background: "#fef1f1",
            fontSize: 18, fontWeight: 700, cursor: "pointer", fontFamily: "'Heebo', sans-serif", color: "#c62828",
          }}>❌ פתיחה לא טובה</button>
        </div>
      ) : (
        <div>
          <div style={{
            padding: "12px 16px", borderRadius: 12, marginBottom: 12,
            background: answered.correct ? "#e8f5e9" : "#ffebee",
            border: `1px solid ${answered.correct ? "#a5d6a7" : "#ef9a9a"}`,
          }}>
            <strong style={{ color: answered.correct ? "#2e7d32" : "#c62828" }}>
              {answered.correct ? "🎉 נכון!" : "❌ לא בדיוק..."}
            </strong>
            <p style={{ margin: "6px 0 0", fontSize: 17, color: "#3a3a4a", lineHeight: 1.8 }}>{answered.explanation}</p>
          </div>
          <Button onClick={next} variant="primary" style={{ fontSize: 15 }}>
            {current + 1 >= total ? "סיום התרגול ←" : "הבא ←"}
          </Button>
        </div>
      )}
    </div>
  );
}

function QuizClaims({ onComplete }) {
  const [current, setCurrent] = useState(0);
  const [answered, setAnswered] = useState({});
  const [score, setScore] = useState(0);
  const shuffled = useRef([...CLAIM_QUIZ].sort(() => Math.random() - 0.5).slice(0, 4));
  const q = shuffled.current[current];
  const total = shuffled.current.length;

  const answer = (userSaidGood) => {
    const correct = userSaidGood === q.isGood;
    setAnswered({ correct, explanation: q.explanation });
    if (correct) setScore(s => s + 1);
  };
  const next = () => {
    setAnswered({});
    if (current + 1 >= total) { onComplete(score); return; }
    setCurrent(c => c + 1);
  };

  return (
    <div style={{ background: "#f8f0ff", borderRadius: 16, padding: "20px 24px", marginBottom: 20, border: "1px solid #e0c8f0" }}>
      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 14 }}>
        <h3 style={{ fontSize: 18, color: "#7b1fa2", margin: 0 }}>🎮 תרגול: האם זו טענה טובה?</h3>
        <span style={{ fontSize: 14, color: "#a080c0" }}>{current + 1}/{total}</span>
      </div>
      <div style={{
        background: "#fff", borderRadius: 12, padding: "16px 20px", marginBottom: 14,
        border: "1px solid #e8d8f0", fontSize: 20, lineHeight: 1.9, color: "#2a1a4a",
      }}>
        "{q.text}"
      </div>
      {!answered.correct && answered.correct !== false ? (
        <div style={{ display: "flex", gap: 12 }}>
          <button onClick={() => answer(true)} style={{
            flex: 1, padding: "14px", borderRadius: 12, border: "2px solid #a5d6a7", background: "#f1f8f1",
            fontSize: 18, fontWeight: 700, cursor: "pointer", fontFamily: "'Heebo', sans-serif", color: "#2e7d32",
          }}>✅ טענה טובה</button>
          <button onClick={() => answer(false)} style={{
            flex: 1, padding: "14px", borderRadius: 12, border: "2px solid #ef9a9a", background: "#fef1f1",
            fontSize: 18, fontWeight: 700, cursor: "pointer", fontFamily: "'Heebo', sans-serif", color: "#c62828",
          }}>❌ טענה לא טובה</button>
        </div>
      ) : (
        <div>
          <div style={{
            padding: "12px 16px", borderRadius: 12, marginBottom: 12,
            background: answered.correct ? "#e8f5e9" : "#ffebee",
            border: `1px solid ${answered.correct ? "#a5d6a7" : "#ef9a9a"}`,
          }}>
            <strong style={{ color: answered.correct ? "#2e7d32" : "#c62828" }}>
              {answered.correct ? "🎉 נכון!" : "❌ לא בדיוק..."}
            </strong>
            <p style={{ margin: "6px 0 0", fontSize: 17, color: "#3a3a4a", lineHeight: 1.8 }}>{answered.explanation}</p>
          </div>
          <Button onClick={next} variant="primary" style={{ fontSize: 15 }}>
            {current + 1 >= total ? "סיום התרגול ←" : "הבא ←"}
          </Button>
        </div>
      )}
    </div>
  );
}

function QuizArguments({ onComplete }) {
  const [selected, setSelected] = useState({});
  const [showResults, setShowResults] = useState(false);
  const d = ARGUMENT_QUIZ_DATA;

  const check = () => setShowResults(true);
  const score = Object.entries(selected).filter(([i, v]) => v === d.arguments[i].supports).length;

  return (
    <div style={{ background: "#f0faf8", borderRadius: 16, padding: "20px 24px", marginBottom: 20, border: "1px solid #c0e0d8" }}>
      <h3 style={{ fontSize: 18, color: "#00695c", margin: "0 0 8px" }}>🎮 תרגול: אילו נימוקים תומכים בטענה?</h3>
      <p style={{ fontSize: 16, color: "#3a6a5a", margin: "0 0 14px", lineHeight: 1.6 }}>
        <strong>הטענה:</strong> "{d.claim}"<br />סמנו לכל נימוק: האם הוא <strong>תומך</strong> בטענה או <strong>לא תומך</strong>?
      </p>
      {d.arguments.map((arg, i) => (
        <div key={i} style={{
          background: "#fff", borderRadius: 12, padding: "12px 16px", marginBottom: 10,
          border: showResults
            ? `2px solid ${selected[i] === arg.supports ? "#66bb6a" : "#ef5350"}`
            : "1px solid #d0e8e0",
        }}>
          <p style={{ fontSize: 18, color: "#2a4a3a", margin: "0 0 8px" }}>"{arg.text}"</p>
          <div style={{ display: "flex", gap: 8 }}>
            <button onClick={() => !showResults && setSelected({ ...selected, [i]: true })}
              style={{
                padding: "8px 18px", borderRadius: 10, fontSize: 15, cursor: showResults ? "default" : "pointer",
                fontFamily: "'Heebo', sans-serif", fontWeight: 600,
                background: selected[i] === true ? "#c8e6c9" : "#f5f5f5",
                border: selected[i] === true ? "2px solid #66bb6a" : "1px solid #ddd", color: "#2e7d32",
              }}>תומך 👍</button>
            <button onClick={() => !showResults && setSelected({ ...selected, [i]: false })}
              style={{
                padding: "8px 18px", borderRadius: 10, fontSize: 15, cursor: showResults ? "default" : "pointer",
                fontFamily: "'Heebo', sans-serif", fontWeight: 600,
                background: selected[i] === false ? "#ffcdd2" : "#f5f5f5",
                border: selected[i] === false ? "2px solid #ef5350" : "1px solid #ddd", color: "#c62828",
              }}>לא תומך 👎</button>
          </div>
          {showResults && (
            <p style={{
              margin: "8px 0 0", fontSize: 15, lineHeight: 1.7,
              color: selected[i] === arg.supports ? "#2e7d32" : "#c62828",
            }}>
              {selected[i] === arg.supports ? "✅ " : "❌ "}{arg.explanation}
            </p>
          )}
        </div>
      ))}
      {!showResults ? (
        <Button onClick={check} disabled={Object.keys(selected).length < d.arguments.length}
          style={{ marginTop: 8, fontSize: 15 }}>
          בדיקה ←
        </Button>
      ) : (
        <div>
          <p style={{ fontSize: 18, color: "#00695c", fontWeight: 700, margin: "10px 0" }}>
            ציון: {score}/{d.arguments.length} 🌟
          </p>
          <Button onClick={() => onComplete(score)} style={{ fontSize: 15 }}>סיום התרגול ←</Button>
        </div>
      )}
    </div>
  );
}

function QuizConnectors({ onComplete }) {
  const [answers, setAnswers] = useState({});
  const [showResults, setShowResults] = useState(false);
  const shuffled = useRef([...CONNECTOR_QUIZ].sort(() => Math.random() - 0.5).slice(0, 8));
  const categories = ["beginning", "reason", "addition", "summary"];
  const catNames = { beginning: "🔢 התחלה/סדר", reason: "❓ סיבה", addition: "➕ הוספה", summary: "🎯 סיכום" };

  const check = () => setShowResults(true);
  const score = Object.entries(answers).filter(([i, v]) => v === shuffled.current[i].category).length;

  return (
    <div style={{ background: "#fff8f0", borderRadius: 16, padding: "20px 24px", marginBottom: 20, border: "1px solid #f0d8b0" }}>
      <h3 style={{ fontSize: 18, color: "#e65100", margin: "0 0 8px" }}>🎮 תרגול: לאיזה סוג שייכת מילת הקישור?</h3>
      <p style={{ fontSize: 16, color: "#8a6a30", margin: "0 0 14px" }}>לחצו על הקטגוריה המתאימה לכל מילת קישור:</p>
      {shuffled.current.map((item, i) => (
        <div key={i} style={{
          background: "#fff", borderRadius: 12, padding: "12px 16px", marginBottom: 10,
          border: showResults
            ? `2px solid ${answers[i] === item.category ? "#66bb6a" : "#ef5350"}`
            : "1px solid #f0e0c8",
        }}>
          <p style={{ fontSize: 19, fontWeight: 600, color: "#3a2a1a", margin: "0 0 8px" }}>"{item.word}"</p>
          <div style={{ display: "flex", gap: 6, flexWrap: "wrap" }}>
            {categories.map(cat => (
              <button key={cat} onClick={() => !showResults && setAnswers({ ...answers, [i]: cat })}
                style={{
                  padding: "7px 16px", borderRadius: 10, fontSize: 15, cursor: showResults ? "default" : "pointer",
                  fontFamily: "'Heebo', sans-serif", fontWeight: 600,
                  background: answers[i] === cat ? "#e8dff5" : "#f8f8f8",
                  border: answers[i] === cat ? "2px solid #7c5cbf" : "1px solid #ddd",
                  color: "#5a3e8e",
                }}>
                {catNames[cat]}
              </button>
            ))}
          </div>
          {showResults && (
            <p style={{ margin: "6px 0 0", fontSize: 14, color: answers[i] === item.category ? "#2e7d32" : "#c62828" }}>
              {answers[i] === item.category ? "✅ נכון!" : `❌ התשובה: ${catNames[item.category]}`}
            </p>
          )}
        </div>
      ))}
      {!showResults ? (
        <Button onClick={check} disabled={Object.keys(answers).length < shuffled.current.length}
          variant="secondary" style={{ marginTop: 8, fontSize: 15 }}>בדיקה ←</Button>
      ) : (
        <div>
          <p style={{ fontSize: 14, color: "#e65100", fontWeight: 700, margin: "10px 0" }}>ציון: {score}/{shuffled.current.length} 🌟</p>
          <Button onClick={() => onComplete(score)} variant="secondary" style={{ fontSize: 15 }}>סיום ←</Button>
        </div>
      )}
    </div>
  );
}

// ==================== STAGES ====================

function Stage0_TopicSelect({ data, setData, onNext }) {
  return (
    <StageCard title="בחירת נושא" icon="📋" color="#6a4fa0">
      <InfoBox type="info">
        <strong>ברוכים הבאים ללומדת הכתיבה הטיעונית!</strong><br />
        בלומדה זו תלמדו לכתוב טקסט טיעוני שלב אחר שלב, בשיטת <strong>פטנד"ס</strong>: פתיחה, טענה, נימוקים, דוגמאות, סיכום.<br />
        בואו נתחיל בבחירת נושא!
      </InfoBox>
      <p style={{ fontSize: 15, color: "#5a3e8e", marginBottom: 14, lineHeight: 1.7 }}>בחרו נושא שמעניין אתכם:</p>
      <div style={{ display: "grid", gap: 10 }}>
        {TOPICS.map(t => (
          <button key={t.id} onClick={() => setData({ ...data, topic: t, customTopic: t.id === "custom" ? data.customTopic : "" })}
            style={{
              padding: "14px 18px", borderRadius: 14, textAlign: "right",
              border: data.topic?.id === t.id ? "2px solid #6a4fa0" : "2px solid #e8e0f0",
              background: data.topic?.id === t.id ? "linear-gradient(135deg, #f5f0ff, #ece4ff)" : "#faf8ff",
              cursor: "pointer", fontSize: 15, fontFamily: "'Heebo', sans-serif",
              color: t.id === "custom" ? "#e65100" : "#3d2a5c", transition: "all 0.3s",
              fontWeight: t.id === "custom" ? 700 : 400,
              boxShadow: data.topic?.id === t.id ? "0 3px 12px rgba(106,79,160,0.12)" : "none",
            }}>
            {t.id === "custom" ? "✨ " : ""}{t.title}
          </button>
        ))}
      </div>
      {data.topic?.id === "custom" && (
        <div style={{ marginTop: 14 }}>
          <TextArea
            value={data.customTopic || ""}
            onChange={v => setData({ ...data, customTopic: v })}
            placeholder="כתבו כאן את הנושא שלכם בצורת שאלה, למשל: האם יש ל...?"
            rows={2}
            label="כתבו את הנושא שלכם:"
          />
        </div>
      )}
      <div style={{ display: "flex", justifyContent: "flex-start", marginTop: 20 }}>
        <Button onClick={() => {
          if (data.topic?.id === "custom" && data.customTopic?.trim()) {
            setData({ ...data, topic: { id: "custom", title: data.customTopic, short: data.customTopic.slice(0, 20) } });
          }
          onNext();
        }} disabled={!data.topic || (data.topic.id === "custom" && !data.customTopic?.trim())}>
          נתחיל! ←
        </Button>
      </div>
    </StageCard>
  );
}

function QuizGeneralizations({ onComplete }) {
  const allRounds = [
    [
      { specific: "ילדים מצלמים מורים בזמן שיעור", options: ["שימוש לרעה בטלפונים בזמן שיעור", "מורים לא אוהבים צילומים", "ילדים שובבים"], correct: 0 },
      { specific: "חבר שלי נפגע מתגובות מכוערות באינסטגרם", options: ["אינסטגרם אפליקציה רעה", "בריונות רשת בקרב בני נוער", "חברים לא נחמדים"], correct: 1 },
      { specific: "אחי תמיד על הטיקטוק במקום לעשות שיעורי בית", options: ["טיקטוק ממכר", "פגיעה בריכוז ובהקצאת זמן ללמידה", "אחים מעצבנים"], correct: 1 },
      { specific: "תלמיד בכיתה שלנו העתיק תשובות מוואטסאפ", options: ["וואטסאפ לא מתאים לילדים", "העתקות והונאות באמצעות טכנולוגיה", "תלמידים עצלנים"], correct: 1 },
      { specific: "אני משתמש באפליקציה שעוזרת לי ללמוד אנגלית", options: ["אפליקציות טובות", "שימוש בטכנולוגיה ככלי למידה והעשרה", "אנגלית קשה"], correct: 1 },
    ],
    [
      { specific: "ילד בכיתה שלנו לא מפסיק להסתכל על הטלפון", options: ["ילדים לא מקשיבים", "התמכרות למסכים בקרב בני נוער", "טלפונים מעניינים"], correct: 1 },
      { specific: "אמא שלי לא נותנת לי טלפון עד גיל 14", options: ["הורים מחמירים מדי", "הגבלת גישה לטכנולוגיה בגיל צעיר", "אמהות שולטניות"], correct: 1 },
      { specific: "חבר שלי מצא מידע לפרויקט דרך יוטיוב", options: ["יוטיוב אתר טוב", "נגישות למידע ולמשאבי למידה דיגיטליים", "פרויקטים קלים"], correct: 1 },
      { specific: "ראיתי שבזמן הפסקה כולם יושבים ומשחקים בטלפון", options: ["הפסקות משעממות", "צמצום האינטראקציה החברתית פנים אל פנים", "משחקים כיפיים"], correct: 1 },
      { specific: "תלמידה שלחה הודעה פוגענית בקבוצת הכיתה", options: ["תלמידות רעות", "פגיעה באקלים הכיתתי באמצעות תקשורת דיגיטלית", "קבוצות וואטסאפ מסוכנות"], correct: 1 },
    ],
    [
      { specific: "הבן שלי למד לבשל מסרטונים באינטרנט", options: ["בישול קל", "למידה עצמאית באמצעות תוכן דיגיטלי", "ילדים חכמים"], correct: 1 },
      { specific: "בכיתה שלנו מורה תפס תלמיד מצלם בבחינה", options: ["מורים צודקים", "שימוש בטכנולוגיה לרמאות במבחנים", "תלמידים לא מוכנים"], correct: 1 },
      { specific: "חברה שלי לא ישנה בלילה בגלל שהיא גולשת ברשת", options: ["רשתות חברתיות גרועות", "פגיעה בבריאות הגופנית עקב שימוש מופרז בטכנולוגיה", "ילדות לא ישנות"], correct: 1 },
      { specific: "אבא שלי עוזר לי לתרגל חשבון עם אפליקציה", options: ["אבות טובים", "שיתוף פעולה בין הורים לילדים באמצעות כלים דיגיטליים", "חשבון קשה"], correct: 1 },
      { specific: "מישהו פרסם תמונה שלי בלי רשות", options: ["אנשים לא נחמדים", "פגיעה בפרטיות ובזכויות הפרט במרחב הדיגיטלי", "תמונות מביכות"], correct: 1 },
    ],
  ];

  const [round, setRound] = useState(0);
  const [answers, setAnswers] = useState({});
  const [checked, setChecked] = useState(false);
  const [totalScore, setTotalScore] = useState(0);
  const [totalDone, setTotalDone] = useState(0);

  const items = allRounds[round];
  const score = Object.entries(answers).filter(([i, v]) => v === items[i].correct).length;

  const nextRound = () => {
    setTotalScore(prev => prev + score);
    setTotalDone(prev => prev + items.length);
    if (round + 1 < allRounds.length) {
      setRound(r => r + 1);
      setAnswers({});
      setChecked(false);
    }
  };

  const finishAll = () => {
    onComplete();
  };

  return (
    <div style={{ background: "#fff8e1", borderRadius: 16, padding: "20px 24px", marginBottom: 20, border: "2px solid #ffe082" }}>
      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 6 }}>
        <h3 style={{ fontSize: 18, color: "#f57f17", margin: 0 }}>🎮 תרגול: התאימו דוגמה להכללה!</h3>
        <span style={{ fontSize: 14, color: "#9a8a40", background: "#fff3d0", padding: "3px 10px", borderRadius: 10, fontWeight: 600 }}>
          סבב {round + 1} מתוך {allRounds.length}
        </span>
      </div>
      <p style={{ fontSize: 16, color: "#7a6a20", margin: "0 0 16px", lineHeight: 1.6 }}>
        לכל דוגמה ספציפית, בחרו את ההכללה שמתארת את <strong>התופעה הכללית</strong> שהיא מייצגת:
      </p>
      {items.map((item, i) => (
        <div key={i} style={{
          background: "#fff", borderRadius: 12, padding: "14px 16px", marginBottom: 12,
          border: checked ? `2px solid ${answers[i] === item.correct ? "#66bb6a" : "#ef5350"}` : "1px solid #ffe0a0",
        }}>
          <p style={{ fontSize: 16, color: "#c62828", margin: "0 0 8px", fontWeight: 600 }}>
            ❌ דוגמה ספציפית: "{item.specific}"
          </p>
          <p style={{ fontSize: 16, color: "#5a4a10", margin: "0 0 8px" }}>✅ מה ההכללה?</p>
          <div style={{ display: "flex", flexDirection: "column", gap: 6 }}>
            {item.options.map((opt, j) => (
              <button key={j} onClick={() => !checked && setAnswers({ ...answers, [i]: j })}
                style={{
                  padding: "8px 14px", borderRadius: 10, textAlign: "right", fontSize: 15,
                  fontFamily: "'Heebo', sans-serif", cursor: checked ? "default" : "pointer",
                  background: checked && j === item.correct ? "#c8e6c9"
                    : checked && answers[i] === j && j !== item.correct ? "#ffcdd2"
                    : answers[i] === j ? "#e8f0ff" : "#f8f8f8",
                  border: answers[i] === j ? "2px solid #5c9ce6" : "1px solid #e0d8c8",
                  color: "#3a3a4a", fontWeight: answers[i] === j ? 600 : 400,
                  transition: "all 0.2s",
                }}>
                {checked && j === item.correct ? "✅ " : checked && answers[i] === j && j !== item.correct ? "❌ " : ""}{opt}
              </button>
            ))}
          </div>
        </div>
      ))}
      {!checked ? (
        <Button onClick={() => setChecked(true)} disabled={Object.keys(answers).length < items.length}
          style={{ marginTop: 8, fontSize: 15 }}>
          בדיקה ←
        </Button>
      ) : (
        <div>
          <p style={{ fontSize: 14, color: "#f57f17", fontWeight: 700, margin: "10px 0" }}>
            ציון בסבב הזה: {score}/{items.length} 🌟
            {totalDone > 0 && <span style={{ fontSize: 14, color: "#9a8a40", marginRight: 10 }}> (סה״כ: {totalScore + score}/{totalDone + items.length})</span>}
          </p>
          {score < items.length && (
            <p style={{ fontSize: 16, color: "#7a6a20", margin: "0 0 10px", lineHeight: 1.6 }}>
              💡 הכללה = <strong>תיאור של תופעה רחבה</strong>. לא מקרה פרטי ("חבר שלי...") ולא הערכה כללית מדי ("טלפונים רעים").
            </p>
          )}
          <div style={{ display: "flex", gap: 8 }}>
            {round + 1 < allRounds.length && (
              <Button onClick={nextRound} variant="secondary" style={{ fontSize: 15 }}>
                🔄 סבב נוסף ({round + 2}/{allRounds.length})
              </Button>
            )}
            <Button onClick={finishAll} style={{ fontSize: 15 }}>
              {round + 1 >= allRounds.length ? "סיימתי את כל הסבבים! ←" : "מספיק – בואו נכתוב! ←"}
            </Button>
          </div>
        </div>
      )}
    </div>
  );
}

function Stage1_Draft({ data, setData, onNext, onBack }) {
  const [feedback, setFeedback] = useState(null);
  const [fbLoading, setFbLoading] = useState(false);
  const [showGenExample, setShowGenExample] = useState(false);
  const [quizDone, setQuizDone] = useState(false);
  const [genSuggestions, setGenSuggestions] = useState(null); // AI-generated generalization suggestions

  // Get AI generalization suggestions for specific examples
  const getGeneralizationSuggestions = async (specificText, argIndex, argSide) => {
    try {
      const response = await fetch("https://api.anthropic.com/v1/messages", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          model: "claude-sonnet-4-20250514",
          max_tokens: 1000,
          system: `אתה מורה לכתיבה טיעונית. התלמיד כתב דוגמה ספציפית במקום הכללה. 
תפקידך: להציע 3 אפשרויות הכללה שונות שהדוגמה הספציפית שלו יכולה לייצג.
הנושא: "${data.topic?.title || ""}"

חוקים:
- כל הכללה היא ביטוי קצר (3-8 מילים) שמתאר תופעה רחבה
- ההכללות צריכות להיות שונות זו מזו ברמת ההפשטה או בזווית
- אל תכתוב משפט שלם, רק ביטוי מכליל
- ענה בפורמט JSON בלבד, בלי backticks:
{"suggestions":["הכללה 1","הכללה 2","הכללה 3"]}`,
          messages: [{ role: "user", content: `הדוגמה הספציפית שכתב התלמיד: "${specificText}"` }],
        }),
      });
      const d = await response.json();
      const text = d.content?.map(c => c.text || "").join("") || "";
      const clean = text.replace(/```json|```/g, "").trim();
      const parsed = JSON.parse(clean);
      return { suggestions: parsed.suggestions, argIndex, argSide };
    } catch {
      return null;
    }
  };

  const getFb = async () => {
    const pros = (data.prosArguments || []).filter(a => a.trim());
    const cons = (data.consArguments || []).filter(a => a.trim());
    if (pros.length === 0 && cons.length === 0) return;
    
    setFbLoading(true);
    setGenSuggestions(null);
    
    // === LOCAL CHECKS: duplicates & specific examples ===
    const normalize = (s) => s.trim().replace(/[.,!?]/g, "").toLowerCase();
    const getWords = (s) => normalize(s).split(/\s+/).filter(w => w.length > 2);
    const areSimilar = (a, b) => {
      const na = normalize(a); const nb = normalize(b);
      if (na === nb) return true;
      if (na.includes(nb) || nb.includes(na)) return true;
      const wa = getWords(a); const wb = getWords(b);
      if (wa.length === 0 || wb.length === 0) return false;
      return wa.filter(w => wb.includes(w)).length / Math.min(wa.length, wb.length) >= 0.6;
    };
    
    const localParts = [];
    
    // Duplicate detection
    const dupFound = [];
    for (let i = 0; i < pros.length; i++) {
      for (let j = i + 1; j < pros.length; j++) {
        if (areSimilar(pros[i], pros[j])) dupFound.push(`🔄 בעד: "${pros[i]}" ו-"${pros[j]}" – אותו רעיון!`);
      }
    }
    for (let i = 0; i < cons.length; i++) {
      for (let j = i + 1; j < cons.length; j++) {
        if (areSimilar(cons[i], cons[j])) dupFound.push(`🔄 נגד: "${cons[i]}" ו-"${cons[j]}" – אותו רעיון!`);
      }
    }
    for (let i = 0; i < pros.length; i++) {
      for (let j = 0; j < cons.length; j++) {
        if (areSimilar(pros[i], cons[j])) dupFound.push(`🔄 בעד ונגד: "${pros[i]}" ו-"${cons[j]}" – אותו רעיון!`);
      }
    }
    if (dupFound.length > 0) {
      localParts.push("⚠️ יש רעיונות שחוזרים על עצמם!");
      localParts.push(...dupFound);
    }
    
    // Specific example detection + AI generalization suggestions
    const specificPatterns = [
      /חבר שלי/i, /אח[ותי]? שלי/i, /אמא שלי/i, /אבא שלי/i, /המורה שלי/i, /הבת שלי/i, /הבן שלי/i,
      /פעם אחת/i, /יום אחד/i, /פעם ש/i, /כשהייתי/i, /קרה לי/i, /ראיתי ש/i, /שמעתי ש/i,
      /ילד אחד/i, /תלמיד אחד/i, /בן אדם אחד/i, /מישהו ש/i,
      /בבית ספר שלנו/i, /בכיתה שלנו/i, /אצלנו/i,
      /למשל אני/i, /אני תמיד/i, /אני אף פעם/i,
      /מצלמ/i, /מעתיק/i, /משחק/i, /יושב על/i, /גולש ב/i, /צופ[הה] ב/i,
      /סיפור/i, /מקרה/i, /אירוע/i,
    ];
    
    const allSpecifics = [];
    pros.forEach((arg, i) => {
      if (specificPatterns.some(p => p.test(arg))) allSpecifics.push({ text: arg, index: i, side: "pro" });
    });
    cons.forEach((arg, i) => {
      if (specificPatterns.some(p => p.test(arg))) allSpecifics.push({ text: arg, index: i, side: "con" });
    });
    
    if (allSpecifics.length > 0) {
      localParts.push(`⚠️ מצאתי ${allSpecifics.length === 1 ? "דוגמה ספציפית" : allSpecifics.length + " דוגמאות ספציפיות"}! בטיוטה כותבים הכללות.`);
      localParts.push("🔑 בחרו הכללה מתאימה:");
      const suggestions = [];
      for (const spec of allSpecifics.slice(0, 3)) {
        const result = await getGeneralizationSuggestions(spec.text, spec.index, spec.side);
        if (result) suggestions.push({ ...result, originalText: spec.text });
      }
      setGenSuggestions(suggestions);
    }
    
    // === ALWAYS run AI for content depth analysis ===
    const content = `נימוקים בעד:\n${pros.map((a, i) => `${i + 1}. ${a}`).join("\n")}\n\nנימוקים נגד:\n${cons.map((a, i) => `${i + 1}. ${a}`).join("\n")}`;
    const aiFb = await getAIFeedback("draft", content, data.topic?.title);
    
    // Combine: local warnings first, then AI depth analysis
    if (localParts.length > 0) {
      setFeedback(localParts.join("\n") + "\n\n" + aiFb);
    } else {
      setFeedback(aiFb);
    }
    setFbLoading(false);
  };

  const applyGeneralization = (argSide, argIndex, newText) => {
    if (argSide === "pro") {
      const a = [...(data.prosArguments || ["", "", ""])]; a[argIndex] = newText;
      setData({ ...data, prosArguments: a });
    } else {
      const a = [...(data.consArguments || ["", "", ""])]; a[argIndex] = newText;
      setData({ ...data, consArguments: a });
    }
    // Remove this suggestion from the list
    setGenSuggestions(prev => prev?.filter(s => !(s.argIndex === argIndex && s.argSide === argSide)));
  };

  const hasEnoughArgs = (data.prosArguments?.filter(a => a.trim()).length >= 1 || data.consArguments?.filter(a => a.trim()).length >= 1);

  return (
    <StageCard title="שלב הטיוטה – הבנת המשימה" icon="📝" color="#e8853a">
      <InfoBox type="info">
        <strong>לפני שמתחילים לכתוב</strong>, חשוב להבין את הנושא ולחשוב על נימוקים <strong>בעד</strong> ונימוקים <strong>נגד</strong>.<br />
        זה יעזור לכם לבנות טקסט חזק ומשכנע!
      </InfoBox>

      {/* Generalization teaching section */}
      <div style={{
        background: "linear-gradient(135deg, #fff8e1, #fff3d0)", borderRadius: 16,
        padding: "18px 22px", marginBottom: 20, border: "2px solid #ffe082",
      }}>
        <h3 style={{ fontSize: 18, color: "#f57f17", margin: "0 0 10px", display: "flex", alignItems: "center", gap: 8 }}>
          <span style={{ fontSize: 22 }}>🔑</span> מיומנות חשובה: כתיבת הכללות
        </h3>
        <p style={{ fontSize: 16, color: "#5a4a10", margin: "0 0 12px", lineHeight: 1.8 }}>
          בטיוטה אנחנו לא כותבים דוגמאות ספציפיות, אלא <strong>רעיונות כלליים ומכלילים</strong>.<br />
          הכללה = ביטוי שמתאר תופעה רחבה, לא מקרה אחד מסוים.
        </p>

        <div style={{ background: "#fff", borderRadius: 12, padding: "14px 18px", border: "1px solid #ffe0a0", marginBottom: 12 }}>
          <div style={{ display: "grid", gridTemplateColumns: "1fr auto 1fr", gap: 10, alignItems: "center" }}>
            <div style={{ background: "#ffebee", borderRadius: 10, padding: "10px 14px" }}>
              <p style={{ fontSize: 11, color: "#c62828", margin: "0 0 4px", fontWeight: 700 }}>❌ דוגמה ספציפית:</p>
              <p style={{ fontSize: 16, color: "#5a2020", margin: 0 }}>"ילדים מצלמים מורים"</p>
            </div>
            <span style={{ fontSize: 24, color: "#f57f17" }}>➜</span>
            <div style={{ background: "#e8f5e9", borderRadius: 10, padding: "10px 14px" }}>
              <p style={{ fontSize: 11, color: "#2e7d32", margin: "0 0 4px", fontWeight: 700 }}>✅ הכללה:</p>
              <p style={{ fontSize: 16, color: "#1a3a1a", margin: 0 }}>"שימוש לרעה בטלפונים בזמן שיעור"</p>
            </div>
          </div>
        </div>

        <button onClick={() => setShowGenExample(!showGenExample)} style={{
          background: "none", border: "none", color: "#f57f17", cursor: "pointer",
          fontSize: 13, fontFamily: "'Heebo', sans-serif", fontWeight: 700, padding: 0,
        }}>
          {showGenExample ? "הסתר דוגמאות נוספות ▲" : "עוד דוגמאות ▼"}
        </button>

        {showGenExample && (
          <div style={{ marginTop: 10, display: "flex", flexDirection: "column", gap: 8 }}>
            {[
              ["תלמיד העתיק בוואטסאפ", "העתקות והונאות באמצעות טכנולוגיה"],
              ["אחי תמיד על הטיקטוק", "פגיעה בריכוז ובזמן למידה"],
              ["חבר נפגע מבריונות ברשת", "בריונות רשת בקרב בני נוער"],
              ["המורה לא מרשה טלפונים", "הגבלת חירות אישית של תלמידים"],
              ["אפליקציה שעוזרת לי ללמוד", "שימוש בטכנולוגיה ככלי למידה"],
            ].map(([specific, general], i) => (
              <div key={i} style={{ display: "flex", gap: 8, alignItems: "center", fontSize: 14 }}>
                <span style={{ color: "#c62828", minWidth: "45%", background: "#fff5f5", padding: "4px 8px", borderRadius: 6 }}>❌ {specific}</span>
                <span style={{ color: "#f57f17" }}>➜</span>
                <span style={{ color: "#2e7d32", background: "#f0f8f0", padding: "4px 8px", borderRadius: 6 }}>✅ {general}</span>
              </div>
            ))}
          </div>
        )}
      </div>

      {/* Matching practice quiz */}
      {!quizDone ? (
        <QuizGeneralizations onComplete={() => setQuizDone(true)} />
      ) : (
        <div style={{ background: "#e8f5e9", borderRadius: 12, padding: "12px 16px", marginBottom: 16, border: "1px solid #a5d6a7" }}>
          <p style={{ fontSize: 16, color: "#2e7d32", margin: 0, fontWeight: 600 }}>✅ סיימתם את תרגול ההכללות! עכשיו כתבו הכללות לנושא שלכם.</p>
        </div>
      )}

      {/* === TOPIC BANNER - prominent, right above writing === */}
      <div style={{
        background: "linear-gradient(135deg, #e8d5f5, #d4b8eb)", borderRadius: "14px 14px 0 0",
        padding: "16px 24px", marginBottom: 0, border: "2px solid #b39ddb",
        borderBottom: "none", textAlign: "center",
        boxShadow: "0 2px 8px rgba(106,79,160,0.15)",
      }}>
        <p style={{ fontSize: 11, color: "#7e57c2", margin: "0 0 4px", fontWeight: 700, letterSpacing: 1, textTransform: "uppercase" }}>📌 כתבו הכללות על הנושא:</p>
        <p style={{ fontSize: 20, fontWeight: 900, color: "#4a148c", margin: 0, lineHeight: 1.3 }}>{data.topic?.title}</p>
      </div>

      <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 0, border: "2px solid #b39ddb", borderTop: "none", borderRadius: "0 0 14px 14px", overflow: "hidden" }}>
        <div style={{ background: "linear-gradient(135deg, #e8f5e9, #f1f8f2)", padding: "16px 18px", borderLeft: "1px solid #d0e0d0" }}>
          <h3 style={{ fontSize: 15, color: "#2e7d32", margin: "0 0 10px" }}>👍 הכללות בעד</h3>
          {[0, 1, 2].map(i => (
            <TextArea key={i} value={data.prosArguments?.[i] || ""}
              onChange={v => { const a = [...(data.prosArguments || ["", "", ""])]; a[i] = v; setData({ ...data, prosArguments: a }); setFeedback(null); setGenSuggestions(null); }}
              placeholder={`הכללה ${i + 1} בעד...`} rows={2} />
          ))}
        </div>
        <div style={{ background: "linear-gradient(135deg, #fbe9e7, #fdf2f0)", padding: "16px 18px", borderRight: "1px solid #e0d0c0" }}>
          <h3 style={{ fontSize: 15, color: "#c62828", margin: "0 0 10px" }}>👎 הכללות נגד</h3>
          {[0, 1, 2].map(i => (
            <TextArea key={i} value={data.consArguments?.[i] || ""}
              onChange={v => { const a = [...(data.consArguments || ["", "", ""])]; a[i] = v; setData({ ...data, consArguments: a }); setFeedback(null); setGenSuggestions(null); }}
              placeholder={`הכללה ${i + 1} נגד...`} rows={2} />
          ))}
        </div>
      </div>

      {hasEnoughArgs && (
        <div style={{ marginTop: 14 }}>
          <Button onClick={getFb} variant="feedback" disabled={fbLoading}
            style={{ fontSize: 15 }}>
            {fbLoading ? "בודק..." : "📝 בדקו את ההכללות שלי"}
          </Button>
        </div>
      )}
      
      {/* Regular feedback */}
      <FeedbackBox feedback={feedback} loading={fbLoading} onRetry={getFb} />

      {/* AI Generalization suggestions - interactive */}
      {genSuggestions && genSuggestions.length > 0 && (
        <div style={{ marginTop: 14 }}>
          {genSuggestions.map((sg, idx) => (
            <div key={idx} style={{
              background: "#fff8e1", borderRadius: 14, padding: "16px 20px", marginBottom: 12,
              border: "2px solid #ffe082",
            }}>
              <p style={{ fontSize: 16, color: "#c62828", margin: "0 0 6px", fontWeight: 600 }}>
                ❌ כתבתם: "{sg.originalText}"
              </p>
              <p style={{ fontSize: 17, color: "#5a4a10", margin: "0 0 10px" }}>
                🔑 בחרו הכללה שמתאימה, או כתבו משלכם:
              </p>
              <div style={{ display: "flex", flexDirection: "column", gap: 6 }}>
                {sg.suggestions.map((s, j) => (
                  <button key={j} onClick={() => applyGeneralization(sg.argSide, sg.argIndex, s)}
                    style={{
                      padding: "10px 16px", borderRadius: 10, textAlign: "right",
                      background: "#e8f5e9", border: "1px solid #a5d6a7",
                      fontSize: 14, fontFamily: "'Heebo', sans-serif", cursor: "pointer",
                      color: "#1b5e20", fontWeight: 500, transition: "all 0.2s",
                    }}
                    onMouseOver={e => { e.target.style.background = "#c8e6c9"; e.target.style.fontWeight = "700"; }}
                    onMouseOut={e => { e.target.style.background = "#e8f5e9"; e.target.style.fontWeight = "500"; }}>
                    ✅ {s}
                  </button>
                ))}
              </div>
            </div>
          ))}
        </div>
      )}

      <InfoBox type="tip">
        <strong>טיפ:</strong> נסו לחשוב על לפחות 2 הכללות בעד ו-2 הכללות נגד! הדוגמאות הספציפיות יבואו בשלב הנימוקים.
      </InfoBox>
      <div style={{ display: "flex", justifyContent: "space-between", marginTop: 20 }}>
        <Button onClick={onBack} variant="outline">→ חזרה</Button>
        <Button onClick={onNext}
          disabled={!(data.prosArguments?.filter(a => a.trim()).length >= 2 && data.consArguments?.filter(a => a.trim()).length >= 2)}>
          המשך ←
        </Button>
      </div>
    </StageCard>
  );
}

function Stage2_Opening({ data, setData, onNext, onBack }) {
  const [showExample, setShowExample] = useState(null);
  const [quizDone, setQuizDone] = useState(false);
  const [feedback, setFeedback] = useState(null);
  const [fbLoading, setFbLoading] = useState(false);

  const getFb = async () => {
    if (!data.opening?.trim()) return;
    setFbLoading(true);
    const fb = await getAIFeedback("opening", data.opening, data.topic?.title);
    setFeedback(fb); setFbLoading(false);
  };

  return (
    <StageCard title="שלב הפתיחה – פ' של פטנד״ס" icon="🚪" color="#1565c0">
      <InfoBox type="info">
        <strong>הפתיחה</strong> היא הפסקה הראשונה. היא צריכה:<br />
        ✦ להציג את <strong>הנושא באופן כללי</strong><br />
        ✦ להציג <strong>דילמה, התלבטות או שאלה</strong> – להראות שיש ויכוח!<br />
        ✦ לעורר עניין אצל הקורא<br />
        ✦ <strong>לא לחשוף</strong> את דעת הכותב!
      </InfoBox>

      {!quizDone ? (
        <QuizOpenings onComplete={() => setQuizDone(true)} />
      ) : (
        <BackToTopicBanner topicTitle={data.topic?.title} sectionName="פתיחה" />
      )}

      <h3 style={{ fontSize: 15, color: "#1565c0", margin: "0 0 12px" }}>בחרו סגנון פתיחה:</h3>
      <div style={{ display: "grid", gap: 10, marginBottom: 18 }}>
        {OPENING_STYLES.map((style, i) => (
          <div key={i} style={{
            borderRadius: 14, border: data.selectedOpeningStyle === i ? "2px solid #1565c0" : "2px solid #e0e8f0",
            background: data.selectedOpeningStyle === i ? "#e8f4ff" : "#fafcff",
            overflow: "hidden", transition: "all 0.3s",
          }}>
            <button onClick={() => setData({ ...data, selectedOpeningStyle: i })}
              style={{
                width: "100%", padding: "14px 18px", textAlign: "right", cursor: "pointer",
                border: "none", background: "transparent", fontFamily: "'Heebo', sans-serif",
                display: "flex", alignItems: "center", gap: 10, fontSize: 14,
              }}>
              <span style={{ fontSize: 22 }}>{style.icon}</span>
              <div>
                <strong style={{ color: "#1a3a5c" }}>{style.name}</strong>
                <p style={{ fontSize: 14, color: "#6a8aaa", margin: "3px 0 0" }}>{style.description}</p>
              </div>
            </button>
            {data.selectedOpeningStyle === i && (
              <div style={{ padding: "0 18px 14px" }}>
                <button onClick={() => setShowExample(showExample === i ? null : i)}
                  style={{
                    background: "#d4e8ff", border: "none", borderRadius: 10, padding: "6px 14px",
                    fontSize: 14, color: "#1565c0", cursor: "pointer", fontFamily: "'Heebo', sans-serif", fontWeight: 600,
                  }}>
                  {showExample === i ? "הסתר דוגמה" : "הצג דוגמה 👀"}
                </button>
                {showExample === i && (
                  <div style={{
                    marginTop: 8, padding: "10px 14px", background: "#fff", borderRadius: 10,
                    border: "1px solid #c8ddf0", fontSize: 14, color: "#3a5a7c", lineHeight: 1.7, fontStyle: "italic",
                  }}>{style.example}</div>
                )}
              </div>
            )}
          </div>
        ))}
      </div>

      {data.selectedOpeningStyle !== undefined && (
        <>
          <InfoBox type="tip">
            <strong>תבנית מוצעת:</strong> {OPENING_STYLES[data.selectedOpeningStyle].template}
          </InfoBox>
          <TextArea value={data.opening || ""} onChange={v => { setData({ ...data, opening: v }); setFeedback(null); }}
            placeholder="כתבו כאן את פסקת הפתיחה שלכם..."
            rows={4} label="כתבו את הפתיחה שלכם:"
            helperText="זכרו: הפתיחה מציגה את הנושא באופן כללי מבלי לחשוף את דעתכם!"
          />
          {data.opening?.trim()?.length > 10 && (
            <Button onClick={getFb} variant="feedback" disabled={fbLoading}
              style={{ fontSize: 15, marginBottom: 8 }}>
              {fbLoading ? "בודק..." : "📝 בדקו את הפתיחה שלי"}
            </Button>
          )}
          <FeedbackBox feedback={feedback} loading={fbLoading} onRetry={getFb} />
        </>
      )}

      <div style={{ display: "flex", justifyContent: "space-between", marginTop: 20 }}>
        <Button onClick={onBack} variant="outline">→ חזרה</Button>
        <Button onClick={onNext} disabled={!data.opening?.trim()}>המשך ←</Button>
      </div>
    </StageCard>
  );
}

function Stage3_Claim({ data, setData, onNext, onBack }) {
  const [quizDone, setQuizDone] = useState(false);
  const [showTip, setShowTip] = useState(false);
  const [feedback, setFeedback] = useState(null);
  const [fbLoading, setFbLoading] = useState(false);

  const getFb = async () => {
    if (!data.claim?.trim()) return;
    setFbLoading(true);
    const fb = await getAIFeedback("claim", data.claim, data.topic?.title, data.claim, data.side);
    setFeedback(fb); setFbLoading(false);
  };

  // Examples from OTHER topics (not the student's) so they learn to formulate independently
  const exampleTopics = {
    "לדעתי": "לדעתי, יש לבטל את שיעורי הבית בבתי הספר.",
    "אני סבור/ה": "אני סבורה שיש חשיבות רבה ללימוד חינוך פיננסי בבתי הספר.",
    "עמדתי היא": "עמדתי היא שאין להגביל את השימוש ברשתות חברתיות לבני נוער.",
    "לאחר בחינת הנושא": "לאחר בחינת הנושא, אני טוענת שיש לאפשר לתלמידים לבחור את מקצועות הלימוד שלהם.",
  };

  const claimStyles = [
    { label: "לדעתי", template: "לדעתי, ...", example: exampleTopics["לדעתי"] },
    { label: "אני סבור/ה", template: "אני סבור/ה ש...", example: exampleTopics["אני סבור/ה"] },
    { label: "עמדתי היא", template: "עמדתי היא ש...", example: exampleTopics["עמדתי היא"] },
    { label: "לאחר בחינת הנושא", template: "לאחר בחינת הנושא, אני טוען/ת ש...", example: exampleTopics["לאחר בחינת הנושא"] },
    { label: "ניסוח חופשי", template: "כתבו בניסוח שלכם...", example: null },
  ];

  return (
    <StageCard title="שלב הטענה – ט' של פטנד״ס" icon="💪" color="#7b1fa2">
      <InfoBox type="info">
        <strong>הטענה</strong> היא המשפט שבו אתם מביעים את <strong>דעתכם האישית</strong>.<br />
        ✦ <strong>ברורה וחד-משמעית</strong><br />
        ✦ <strong>ניתנת לביסוס</strong> בנימוקים ודוגמאות<br />
        ✦ אפשר לנסח אותה <strong>בכמה דרכים</strong> – בחרו את הדרך שנוחה לכם!
      </InfoBox>

      {!quizDone ? (
        <QuizClaims onComplete={() => setQuizDone(true)} />
      ) : (
        <BackToTopicBanner topicTitle={data.topic?.title} sectionName="טענה" />
      )}

      <div style={{ background: "#f8f0ff", borderRadius: 14, padding: "16px 20px", marginBottom: 18, border: "1px solid #e0c8f0" }}>
        <p style={{ fontSize: 15, color: "#6b4fa0", margin: "0 0 6px" }}><strong>הנושא:</strong> {data.topic?.title}</p>
        <p style={{ fontSize: 14, color: "#8a7aaa", margin: 0 }}>
          <strong>בעד:</strong> {data.prosArguments?.filter(a => a.trim()).join(" | ")}
        </p>
        <p style={{ fontSize: 14, color: "#8a7aaa", margin: "2px 0 0" }}>
          <strong>נגד:</strong> {data.consArguments?.filter(a => a.trim()).join(" | ")}
        </p>
      </div>

      <label style={{ display: "block", fontWeight: 600, fontSize: 14, color: "#5a3e8e", marginBottom: 8 }}>בחרו צד:</label>
      <div style={{ display: "flex", gap: 12, marginBottom: 16 }}>
        {[["pro", "👍 בעד", "#43a047", "#f0f8f0", "#c8e6c9"], ["con", "👎 נגד", "#e53935", "#fef0f0", "#ffccbc"]].map(([side, label, activeColor, bg, border]) => (
          <button key={side} onClick={() => setData({ ...data, side })}
            style={{
              flex: 1, padding: "12px", borderRadius: 12, fontSize: 15, fontWeight: 700,
              fontFamily: "'Heebo', sans-serif", cursor: "pointer",
              background: data.side === side ? `linear-gradient(135deg, ${activeColor}, ${activeColor}cc)` : bg,
              color: data.side === side ? "#fff" : activeColor,
              border: data.side === side ? "none" : `2px solid ${border}`, transition: "all 0.3s",
            }}>{label}</button>
        ))}
      </div>

      {data.side && (
        <>
          <div style={{
            background: "#faf5ff", borderRadius: 14, padding: "16px 20px", marginBottom: 16,
            border: "1px solid #e8d8f5",
          }}>
            <h4 style={{ fontSize: 14, color: "#7b1fa2", margin: "0 0 10px" }}>🎨 בחרו סגנון ניסוח לטענה:</h4>
            <p style={{ fontSize: 14, color: "#9a7cc0", margin: "0 0 10px" }}>כל דוגמה היא מנושא אחר – אתם תנסחו את הטענה שלכם בנושא שבחרתם!</p>
            <div style={{ display: "grid", gap: 8 }}>
              {claimStyles.map((style, i) => (
                <div key={i} style={{
                  padding: "10px 14px", borderRadius: 10,
                  background: data.selectedClaimStyle === i ? "#ede4f7" : "#fff",
                  border: data.selectedClaimStyle === i ? "2px solid #9c27b0" : "1px solid #e8e0f0",
                  cursor: "pointer", transition: "all 0.2s",
                }} onClick={() => {
                  setData({ ...data, selectedClaimStyle: i });
                }}>
                  <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center" }}>
                    <strong style={{ fontSize: 14, color: "#5a3e8e" }}>{style.label}</strong>
                    <span style={{ fontSize: 13, color: "#a080c0" }}>{style.template}</span>
                  </div>
                  {data.selectedClaimStyle === i && style.example && (
                    <p style={{ fontSize: 13, color: "#7a5aaa", margin: "6px 0 0", lineHeight: 1.5, background: "#f8f2ff", borderRadius: 8, padding: "6px 10px" }}>
                      📌 דוגמה (מנושא אחר): "{style.example}"
                    </p>
                  )}
                </div>
              ))}
            </div>
          </div>

          <ConnectorChips type="claim" onSelect={w => setData({ ...data, claim: (data.claim || "") + w + " " })} />
          <TextArea value={data.claim || ""} onChange={v => { setData({ ...data, claim: v }); setFeedback(null); }}
            placeholder={`עכשיו נסחו את הטענה שלכם בנושא: ${data.topic?.title || ""}...`} rows={3} label="✍️ נסחו את הטענה שלכם:"
            helperText="הסתכלו על הדוגמה למעלה – ועכשיו כתבו משפט דומה בנושא שלכם" />

          {data.claim?.trim()?.length > 5 && (
            <Button onClick={getFb} variant="feedback" disabled={fbLoading}
              style={{ fontSize: 15, marginBottom: 8 }}>
              {fbLoading ? "בודק..." : "📝 בדקו את הטענה שלי"}
            </Button>
          )}
          <FeedbackBox feedback={feedback} loading={fbLoading} onRetry={getFb} />

          <button onClick={() => setShowTip(!showTip)} style={{
            background: "none", border: "none", color: "#7b1fa2", cursor: "pointer",
            fontSize: 13, fontFamily: "'Heebo', sans-serif", fontWeight: 600, padding: 0, marginTop: 8,
          }}>
            {showTip ? "הסתר עזרה" : "צריכים עזרה? 💡"}
          </button>
          {showTip && (
            <InfoBox type="tip">
              <strong>דרכים שונות לנסח טענה:</strong><br />
              "לדעתי, יש לאסור שימוש בטלפונים ניידים בבתי ספר."<br />
              "אני סבור/ה שאין מקום לטלפונים בכיתה."<br />
              "עמדתי היא שטלפונים ניידים פוגעים בלמידה ויש לאסור אותם."<br />
              "לאחר בחינת הנושא, אני טוענת שיש להנהיג מדי בית ספר."<br />
              "ביטול שיעורי הבית יביא תועלת רבה לתלמידים – זו עמדתי."
            </InfoBox>
          )}
        </>
      )}

      <div style={{ display: "flex", justifyContent: "space-between", marginTop: 20 }}>
        <Button onClick={onBack} variant="outline">→ חזרה</Button>
        <Button onClick={onNext} disabled={!data.claim?.trim() || !data.side}>המשך ←</Button>
      </div>
    </StageCard>
  );
}

function Stage4_Arguments({ data, setData, onNext, onBack }) {
  const [quizDone, setQuizDone] = useState(false);
  const [connectorQuizDone, setConnectorQuizDone] = useState(false);
  const [feedback, setFeedback] = useState(null);
  const [fbLoading, setFbLoading] = useState(false);

  const relevantArgs = data.side === "pro" ? data.prosArguments : data.consArguments;
  const args = data.detailedArguments || [
    { argument: relevantArgs?.[0] || "", example: "" },
    { argument: relevantArgs?.[1] || "", example: "" },
  ];

  const updateArg = (i, field, v) => {
    const u = [...args]; u[i] = { ...u[i], [field]: v };
    setData({ ...data, detailedArguments: u });
  };
  const addArg = () => setData({ ...data, detailedArguments: [...args, { argument: "", example: "" }] });

  const getFb = async () => {
    const draftArgs = relevantArgs?.filter(a => a?.trim()) || [];
    const draftInfo = draftArgs.length > 0 
      ? `\n\nהכללות מהטיוטה:\n${draftArgs.map((a, i) => `${i + 1}. ${a}`).join("\n")}`
      : "";
    const content = args.map((a, i) => `נימוק ${i + 1}: ${a.argument}\nדוגמה/הסבר: ${a.example}`).join("\n\n") + draftInfo;
    setFbLoading(true);
    const fb = await getAIFeedback("arguments", content, data.topic?.title, data.claim, data.side);
    setFeedback(fb); setFbLoading(false);
  };

  return (
    <StageCard title="נימוקים ודוגמאות – נד״ס של פטנד״ס" icon="📚" color="#00897b">
      <InfoBox type="info">
        <strong>גוף הטקסט</strong> כולל את <strong>הנימוקים</strong> שתומכים בטענה.<br />
        ✦ נימוק = <strong>סיבה</strong> שתומכת בטענה<br />
        ✦ דוגמה = <strong>הוכחה</strong> מהחיים, ממחקר, מהניסיון
      </InfoBox>

      {!quizDone ? (
        <QuizArguments onComplete={() => setQuizDone(true)} />
      ) : !connectorQuizDone ? (
        <QuizConnectors onComplete={() => setConnectorQuizDone(true)} />
      ) : (
        <BackToTopicBanner topicTitle={data.topic?.title} sectionName="נימוקים והדוגמאות" />
      )}

      {/* Show draft ideas as reference + explain reformulation */}
      <div style={{
        background: "linear-gradient(135deg, #fff8e1, #fff3d0)", borderRadius: 14,
        padding: "16px 20px", marginBottom: 18, border: "1px solid #ffe082",
      }}>
        <h4 style={{ fontSize: 14, color: "#f57f17", margin: "0 0 8px", display: "flex", alignItems: "center", gap: 8 }}>
          <span style={{ fontSize: 18 }}>💡</span> חשוב!
        </h4>
        <p style={{ fontSize: 16, color: "#5a4a10", margin: "0 0 10px", lineHeight: 1.7 }}>
          בשלב הטיוטה רשמתם <strong>רעיונות כלליים</strong> לנימוקים. עכשיו הגיע הזמן <strong>לנסח אותם כמשפטים שלמים ומסודרים</strong> – כאלה שמתאימים להיכנס לטקסט הטיעוני.
        </p>
        <div style={{ background: "#fff", borderRadius: 10, padding: "12px 16px", border: "1px solid #ffe0a0" }}>
          <p style={{ fontSize: 13, color: "#8a6a10", margin: "0 0 6px", fontWeight: 700 }}>
            הרעיונות שרשמתם בטיוטה ({data.side === "pro" ? "בעד" : "נגד"}):
          </p>
          {(data.side === "pro" ? data.prosArguments : data.consArguments)?.filter(a => a.trim()).map((a, i) => (
            <div key={i} style={{ display: "flex", gap: 8, alignItems: "flex-start", marginBottom: 4 }}>
              <span style={{ color: "#f57f17", fontWeight: 700, fontSize: 13 }}>•</span>
              <span style={{ fontSize: 17, color: "#5a4a10" }}>{a}</span>
            </div>
          ))}
        </div>
        <p style={{ fontSize: 13, color: "#8a6a10", margin: "10px 0 0", lineHeight: 1.6 }}>
          ⬇️ <strong>קחו את הרעיונות האלה ונסחו אותם מחדש כמשפטים מלאים</strong>, עם מילות קישור ודוגמאות.
        </p>
      </div>

      <InfoBox type="tip">
        <strong>דוגמה למעבר מרעיון לנימוק מנוסח:</strong><br />
        <span style={{ color: "#e65100" }}>רעיון בטיוטה:</span> "מפריע לריכוז"<br />
        <span style={{ color: "#2e7d32" }}>נימוק מנוסח:</span> "ראשית, שימוש בטלפונים ניידים פוגע בריכוז התלמידים בשיעורים, מפני שהתראות והודעות מסיחות את דעתם מהלמידה."
      </InfoBox>

      {args.map((arg, i) => {
        const draftGeneralization = relevantArgs?.[i]?.trim();
        return (
        <div key={i} style={{
          background: i % 2 === 0 ? "#f0faf8" : "#f8f0fa", borderRadius: 14,
          padding: "16px 18px", marginBottom: 14, border: `1px solid ${i % 2 === 0 ? "#c8e8e0" : "#e8c8e0"}`,
        }}>
          <h4 style={{ fontSize: 18, color: "#00695c", margin: "0 0 8px" }}>נימוק {i + 1}</h4>
          {draftGeneralization && (
            <div style={{
              background: "#fff8e1", borderRadius: 8, padding: "8px 12px", marginBottom: 10,
              border: "1px solid #ffe082", display: "flex", gap: 8, alignItems: "center",
            }}>
              <span style={{ fontSize: 14 }}>📌</span>
              <span style={{ fontSize: 17, color: "#5a4a10" }}>
                <strong>ההכללה מהטיוטה:</strong> {draftGeneralization}
              </span>
            </div>
          )}
          <ConnectorChips type={i === 0 ? "beginning" : "addition"} onSelect={w => updateArg(i, "argument", (arg.argument || "") + w + " ")} />
          <ConnectorChips type="reason" onSelect={w => updateArg(i, "argument", (arg.argument || "") + w + " ")} />
          <TextArea value={arg.argument} onChange={v => { updateArg(i, "argument", v); setFeedback(null); }}
            placeholder={draftGeneralization ? `נסחו את "${draftGeneralization}" כמשפט שלם...` : `כתבו את הנימוק ה-${i + 1}...`} rows={2} />
          <ConnectorChips type="example" onSelect={w => updateArg(i, "example", (arg.example || "") + w + " ")} />
          <TextArea value={arg.example} onChange={v => { updateArg(i, "example", v); setFeedback(null); }}
            placeholder="הוסיפו דוגמה או הסבר שתומך בנימוק..." rows={2} label="דוגמה / הסבר:" />
        </div>
        );
      })}

      {args.length < 4 && (
        <button onClick={addArg} style={{
          width: "100%", padding: "10px", borderRadius: 12, border: "2px dashed #c0d8d0",
          background: "#f8fffc", color: "#00897b", fontSize: 14, cursor: "pointer",
          fontFamily: "'Heebo', sans-serif", fontWeight: 600, marginBottom: 14,
        }}>+ הוסיפו נימוק נוסף</button>
      )}

      {args.every(a => a.argument?.trim() && a.example?.trim()) && (
        <Button onClick={getFb} variant="feedback" disabled={fbLoading}
          style={{ fontSize: 15, marginBottom: 8 }}>
          {fbLoading ? "בודק..." : "📝 בדקו את הנימוקים שלי"}
        </Button>
      )}
      <FeedbackBox feedback={feedback} loading={fbLoading} onRetry={getFb} />

      <div style={{ display: "flex", justifyContent: "space-between", marginTop: 20 }}>
        <Button onClick={onBack} variant="outline">→ חזרה</Button>
        <Button onClick={onNext} disabled={!args.every(a => a.argument?.trim() && a.example?.trim())}>המשך ←</Button>
      </div>
    </StageCard>
  );
}

function Stage5_Summary({ data, setData, onNext, onBack }) {
  const [feedback, setFeedback] = useState(null);
  const [fbLoading, setFbLoading] = useState(false);

  const getFb = async () => {
    if (!data.summary?.trim()) return;
    setFbLoading(true);
    const fb = await getAIFeedback("summary", data.summary, data.topic?.title, data.claim, data.side);
    setFeedback(fb); setFbLoading(false);
  };

  return (
    <StageCard title="סיכום ומסקנה – ס' של פטנד״ס" icon="🎯" color="#e65100">
      <InfoBox type="info">
        <strong>פסקת הסיכום</strong> כוללת:<br />
        ✦ <strong>חזרה על הטענה</strong> במילים אחרות<br />
        ✦ <strong>מסקנה</strong> שנובעת מהנימוקים<br />
        ✦ <strong>המלצה</strong> או קריאה לפעולה
      </InfoBox>
      <ConnectorChips type="summary" onSelect={w => setData({ ...data, summary: (data.summary || "") + w + " " })} />
      <TextArea value={data.summary || ""} onChange={v => { setData({ ...data, summary: v }); setFeedback(null); }}
        placeholder="לסיכום, ... לאור כל האמור, המלצתי היא..." rows={5}
        label="כתבו את פסקת הסיכום:" helperText="חזרו על הטענה במילים אחרות, הסיקו מסקנה, והוסיפו המלצה" />

      {data.summary?.trim()?.length > 10 && (
        <Button onClick={getFb} variant="feedback" disabled={fbLoading}
          style={{ fontSize: 15, marginBottom: 8 }}>
          {fbLoading ? "בודק..." : "📝 בדקו את הסיכום שלי"}
        </Button>
      )}
      <FeedbackBox feedback={feedback} loading={fbLoading} onRetry={getFb} />

      <InfoBox type="tip">
        <strong>טיפ:</strong> אל תוסיפו נימוקים חדשים בסיכום!
      </InfoBox>
      <div style={{ display: "flex", justifyContent: "space-between", marginTop: 20 }}>
        <Button onClick={onBack} variant="outline">→ חזרה</Button>
        <Button onClick={onNext} disabled={!data.summary?.trim()}>צפייה בטקסט המלא ←</Button>
      </div>
    </StageCard>
  );
}

function Stage6_Review({ data, onNext, onBack }) {
  const args = data.detailedArguments || [];
  return (
    <StageCard title="הטקסט הטיעוני שלכם" icon="👁️" color="#5c6bc0">
      <InfoBox type="success">
        <strong>כל הכבוד!</strong> סיימתם לכתוב טקסט טיעוני שלם בשיטת פטנד"ס!
      </InfoBox>
      <div style={{
        background: "#fff", borderRadius: 16, padding: "24px 28px",
        border: "2px solid #c4b5e3", lineHeight: 2, fontSize: 15, color: "#2a1a4a",
        boxShadow: "0 4px 20px rgba(90,62,142,0.08)",
      }}>
        {[
          { label: "פתיחה", bg: "#e8f4ff", color: "#1565c0", text: data.opening },
          { label: "טענה", bg: "#f3e5f5", color: "#7b1fa2", text: data.claim },
          ...args.map((a, i) => ({ label: `נימוק ${i + 1} + דוגמה`, bg: "#e0f2f1", color: "#00695c", text: `${a.argument} ${a.example}` })),
          { label: "סיכום", bg: "#fff3e0", color: "#e65100", text: data.summary },
        ].map((s, i) => (
          <div key={i} style={{ marginBottom: 16 }}>
            <span style={{
              display: "inline-block", background: s.bg, color: s.color,
              padding: "2px 10px", borderRadius: 8, fontSize: 11, fontWeight: 700, marginBottom: 6,
            }}>{s.label}</span>
            <p style={{ margin: 0 }}>{s.text}</p>
          </div>
        ))}
      </div>

      <div style={{ background: "#f5f0ff", borderRadius: 14, padding: "16px 20px", marginTop: 18, border: "1px solid #d0c4e8" }}>
        <h3 style={{ fontSize: 15, color: "#5a3e8e", margin: "0 0 8px" }}>🔍 רשימת בדיקה</h3>
        {["הפתיחה מציגה את הנושא מבלי לחשוף את דעתי", "הטענה ברורה ומובנת", "יש לפחות 2 נימוקים עם דוגמאות",
          "הסיכום חוזר על הטענה ומסיק מסקנה", "השתמשתי במילות קישור"].map((item, i) => (
          <label key={i} style={{ display: "flex", alignItems: "center", gap: 8, marginBottom: 6, fontSize: 13, color: "#4a3a6a", cursor: "pointer" }}>
            <input type="checkbox" style={{ width: 16, height: 16, accentColor: "#6a4fa0" }} /> {item}
          </label>
        ))}
      </div>
      <div style={{ display: "flex", justifyContent: "space-between", marginTop: 20, flexWrap: "wrap", gap: 10 }}>
        <Button onClick={onBack} variant="outline">→ חזרה לעריכה</Button>
        <div style={{ display: "flex", gap: 10 }}>
          <Button onClick={() => {
            const text = `${data.opening}\n\n${data.claim}\n\n${(data.detailedArguments || []).map((a,i) => `${a.argument}\n${a.example}`).join("\n\n")}\n\n${data.summary}`;
            navigator.clipboard?.writeText(text).then(() => alert("✅ הטקסט הועתק!")).catch(() => alert("לא ניתן להעתיק"));
          }} variant="primary" style={{ background: "linear-gradient(135deg, #00897b, #4db6ac)" }}>📋 העתקה</Button>
          <Button onClick={onNext} variant="secondary">עוברים לחלק ב' – הפרכה! ←</Button>
        </div>
      </div>
    </StageCard>
  );
}

function Stage7_LearnRefutation({ data, onNext, onBack }) {
  return (
    <StageCard title="מהי הפרכה?" icon="🔄" color="#c62828">
      <div style={{
        background: "linear-gradient(135deg, #fff5f5, #fff0f5)", borderRadius: 16,
        padding: "22px 26px", marginBottom: 20, border: "1px solid #f0c0c0",
      }}>
        <h3 style={{ fontSize: 17, color: "#b71c1c", margin: "0 0 12px" }}>ברוכים הבאים לחלק ב'! 🎉</h3>
        <p style={{ fontSize: 14, color: "#5a2a2a", lineHeight: 1.8, margin: 0 }}>
          בכתיבה טיעונית מתקדמת, אנחנו גם מתייחסים לנימוקים של <strong>הצד השני</strong> ומפריכים אותם!
        </p>
      </div>
      <InfoBox type="info">
        <strong>הפרכה</strong> = התייחסות לנימוק של הצד השני + הסבר למה הוא לא מספיק חזק.<br /><br />
        <strong>המבנה:</strong> "אמנם יש הטוענים ש[נימוק], <strong>אולם</strong> [ההסבר שלכם]"
      </InfoBox>
      <div style={{ background: "#fafafa", borderRadius: 14, padding: "18px 22px", marginBottom: 18, border: "1px solid #e0e0e0" }}>
        <h4 style={{ fontSize: 14, color: "#5a3e8e", margin: "0 0 12px" }}>דוגמה:</h4>
        <div style={{ padding: "10px 14px", background: "#ffebee", borderRadius: 10, borderRight: "4px solid #e53935", marginBottom: 10 }}>
          <span style={{ fontSize: 11, fontWeight: 700, color: "#c62828" }}>נימוק של הצד השני:</span>
          <p style={{ margin: "4px 0 0", fontSize: 13, color: "#5a2a2a" }}>"טלפונים ניידים מפריעים לריכוז בשיעורים"</p>
        </div>
        <div style={{ textAlign: "center", fontSize: 20 }}>⬇️</div>
        <div style={{ padding: "10px 14px", background: "#e8f5e9", borderRadius: 10, borderRight: "4px solid #4caf50", marginTop: 10 }}>
          <span style={{ fontSize: 11, fontWeight: 700, color: "#2e7d32" }}>הפרכה:</span>
          <p style={{ margin: "4px 0 0", fontSize: 17, color: "#2a5a2a" }}>
            "אמנם יש הטוענים שטלפונים ניידים מפריעים לריכוז, <strong>אולם</strong> ניתן להשתמש בהם ככלי לימודי יעיל."
          </p>
        </div>
      </div>
      <InfoBox type="tip">
        <strong>מילות קישור להפרכה:</strong> "אמנם... אולם..." | "למרות ש... יש לזכור ש..." | "נכון ש... אך..."
      </InfoBox>
      <div style={{ display: "flex", justifyContent: "space-between", marginTop: 20 }}>
        <Button onClick={onBack} variant="outline">→ חזרה</Button>
        <Button onClick={onNext}>בואו נתרגל! ←</Button>
      </div>
    </StageCard>
  );
}

function Stage8_PracticeRefutation({ data, setData, onNext, onBack }) {
  const [currentEx, setCurrentEx] = useState(0);
  const [showHint, setShowHint] = useState(false);
  const [showAnswer, setShowAnswer] = useState(false);
  const [completed, setCompleted] = useState([]);
  const [feedback, setFeedback] = useState({});
  const [fbLoading, setFbLoading] = useState(false);
  const ex = REFUTATION_EXERCISES[currentEx];
  const answers = data.refutationPractice || {};

  const getFb = async () => {
    const content = answers[`ex${currentEx}`];
    if (!content?.trim()) return;
    setFbLoading(true);
    const fb = await getAIFeedback("refutation", content, ex.topic, ex.claim);
    setFeedback({ ...feedback, [currentEx]: fb }); setFbLoading(false);
  };

  return (
    <StageCard title="תרגול הפרכות" icon="⚔️" color="#e65100">
      <InfoBox type="info">
        קראו את הנימוק של הצד השני ונסו <strong>להפריך</strong> אותו.
      </InfoBox>
      <div style={{ display: "flex", gap: 8, marginBottom: 18 }}>
        {REFUTATION_EXERCISES.map((_, i) => (
          <button key={i} onClick={() => { setCurrentEx(i); setShowHint(false); setShowAnswer(false); }}
            style={{
              flex: 1, padding: "8px", borderRadius: 10, fontSize: 13, fontWeight: 700,
              fontFamily: "'Heebo', sans-serif", cursor: "pointer",
              background: completed.includes(i) ? "linear-gradient(135deg, #43a047, #66bb6a)"
                : i === currentEx ? "linear-gradient(135deg, #e65100, #ff8f00)" : "#f5f0ff",
              color: (completed.includes(i) || i === currentEx) ? "#fff" : "#6b4fa0",
              border: "none", transition: "all 0.3s",
            }}>
            {completed.includes(i) ? "✓ " : ""}תרגיל {i + 1}
          </button>
        ))}
      </div>

      <div style={{ background: "#fff8f0", borderRadius: 14, padding: "18px 22px", marginBottom: 18, border: "1px solid #ffe0b0" }}>
        <p style={{ fontSize: 14, color: "#8a6a30", margin: "0 0 10px" }}><strong>הנושא:</strong> {ex.topic}</p>
        <div style={{ padding: "12px 16px", background: "#ffebee", borderRadius: 10, borderRight: "4px solid #e53935" }}>
          <span style={{ fontSize: 11, fontWeight: 700, color: "#c62828" }}>נימוק שצריך להפריך:</span>
          <p style={{ margin: "4px 0 0", fontSize: 15, fontWeight: 600, color: "#5a2a2a" }}>"{ex.argument}"</p>
        </div>
      </div>

      <button onClick={() => setShowHint(!showHint)} style={{
        background: "#fff3e0", border: "1px solid #ffe0b0", borderRadius: 10,
        padding: "6px 14px", fontSize: 14, color: "#e65100", cursor: "pointer",
        fontFamily: "'Heebo', sans-serif", fontWeight: 600, marginBottom: 10,
      }}>
        {showHint ? "הסתר רמז" : "רמז 💡"}
      </button>
      {showHint && <InfoBox type="tip">{ex.refutationHint}</InfoBox>}

      <ConnectorChips type="refutation" onSelect={w => {
        setData({ ...data, refutationPractice: { ...answers, [`ex${currentEx}`]: (answers[`ex${currentEx}`] || "") + w + " " } });
      }} />
      <TextArea value={answers[`ex${currentEx}`] || ""}
        onChange={v => { setData({ ...data, refutationPractice: { ...answers, [`ex${currentEx}`]: v } }); setFeedback({ ...feedback, [currentEx]: null }); }}
        placeholder="אמנם יש הטוענים ש..., אולם..." rows={4} label="כתבו את ההפרכה שלכם:" />

      <div style={{ display: "flex", gap: 10, flexWrap: "wrap", marginBottom: 14 }}>
        {answers[`ex${currentEx}`]?.trim()?.length > 10 && (
          <Button onClick={getFb} variant="feedback" disabled={fbLoading} style={{ fontSize: 15 }}>
            {fbLoading ? "בודק..." : "📝 בדקו את ההפרכה"}
          </Button>
        )}
        <button onClick={() => setShowAnswer(!showAnswer)} style={{
          background: "#e8f5e9", border: "1px solid #c8e6c9", borderRadius: 10,
          padding: "6px 14px", fontSize: 14, color: "#2e7d32", cursor: "pointer",
          fontFamily: "'Heebo', sans-serif", fontWeight: 600,
        }}>
          {showAnswer ? "הסתר דוגמה" : "דוגמה להפרכה 👀"}
        </button>
        {answers[`ex${currentEx}`]?.trim() && !completed.includes(currentEx) && (
          <Button onClick={() => setCompleted([...completed, currentEx])} variant="success" style={{ padding: "6px 18px", fontSize: 13 }}>
            סיימתי ✓
          </Button>
        )}
      </div>

      <FeedbackBox feedback={feedback[currentEx]} loading={fbLoading} onRetry={getFb} />

      {showAnswer && (
        <div style={{
          background: "#e8f5e9", borderRadius: 12, padding: "12px 16px", marginTop: 10,
          border: "1px solid #c8e6c9", borderRight: "4px solid #4caf50",
        }}>
          <span style={{ fontSize: 11, fontWeight: 700, color: "#2e7d32" }}>דוגמה:</span>
          <p style={{ margin: "4px 0 0", fontSize: 17, color: "#2a5a2a", lineHeight: 1.7 }}>{ex.exampleRefutation}</p>
        </div>
      )}

      <div style={{ display: "flex", justifyContent: "space-between", marginTop: 20 }}>
        <Button onClick={onBack} variant="outline">→ חזרה</Button>
        <Button onClick={onNext} disabled={completed.length < 2}>
          {completed.length < 2 ? `השלימו לפחות 2 (${completed.length}/2)` : "המשך ←"}
        </Button>
      </div>
    </StageCard>
  );
}

function Stage9_FullEssay({ data, setData, onNext, onBack }) {
  const [feedback, setFeedback] = useState(null);
  const [fbLoading, setFbLoading] = useState(false);

  const getFb = async () => {
    const full = `פתיחה: ${data.fullEssayOpening}\n\nטענה: ${data.fullEssayClaim}\n\nנימוקים ודוגמאות: ${data.fullEssayArguments}\n\nהפרכה: ${data.fullEssayRefutation}\n\nסיכום: ${data.fullEssaySummary}`;
    setFbLoading(true);
    const fb = await getAIFeedback("full", full, data.topic?.title, data.fullEssayClaim, data.side);
    setFeedback(fb); setFbLoading(false);
  };

  const allFilled = data.fullEssayOpening?.trim() && data.fullEssayClaim?.trim() && data.fullEssayArguments?.trim() && data.fullEssayRefutation?.trim() && data.fullEssaySummary?.trim();

  return (
    <StageCard title="כתיבה טיעונית מלאה עם הפרכה" icon="✍️" color="#1565c0">
      <InfoBox type="success">
        <strong>השלב האחרון!</strong> כתבו טקסט טיעוני שלם שכולל <strong>הפרכה</strong>.
      </InfoBox>
      <div style={{ background: "#f0f4ff", borderRadius: 14, padding: "16px 20px", marginBottom: 18, border: "1px solid #c0d0f0" }}>
        <h4 style={{ fontSize: 14, color: "#1565c0", margin: "0 0 8px" }}>📐 מבנה הטקסט:</h4>
        {[
          { label: "פתיחה", color: "#1565c0", bg: "#e3f2fd" },
          { label: "טענה", color: "#7b1fa2", bg: "#f3e5f5" },
          { label: "נימוקים + דוגמאות", color: "#00695c", bg: "#e0f2f1" },
          { label: "הפרכה", color: "#c62828", bg: "#ffebee" },
          { label: "סיכום", color: "#e65100", bg: "#fff3e0" },
        ].map((item, i) => (
          <div key={i} style={{
            display: "flex", alignItems: "center", gap: 10, padding: "8px 12px",
            background: item.bg, borderRadius: 8, borderRight: `3px solid ${item.color}`, marginBottom: 6,
          }}>
            <span style={{ fontWeight: 700, fontSize: 13, color: item.color }}>{item.label}</span>
          </div>
        ))}
      </div>

      <TextArea value={data.fullEssayOpening || data.opening || ""}
        onChange={v => { setData({ ...data, fullEssayOpening: v }); setFeedback(null); }}
        rows={3} label="פתיחה:" helperText="תוכלו להשתמש בפתיחה שכתבתם קודם או לכתוב חדשה" />

      <TextArea value={data.fullEssayClaim || data.claim || ""}
        onChange={v => { setData({ ...data, fullEssayClaim: v }); setFeedback(null); }}
        rows={2} label="טענה:" />

      <ConnectorChips type="beginning" onSelect={w => setData({ ...data, fullEssayArguments: (data.fullEssayArguments || "") + w + " " })} />
      <ConnectorChips type="addition" onSelect={w => setData({ ...data, fullEssayArguments: (data.fullEssayArguments || "") + w + " " })} />
      <TextArea value={data.fullEssayArguments || ""}
        onChange={v => { setData({ ...data, fullEssayArguments: v }); setFeedback(null); }}
        rows={6} label="נימוקים ודוגמאות:" />

      <div style={{ background: "#fff5f5", borderRadius: 14, padding: "16px 18px", marginBottom: 14, border: "1px solid #ffc8c8" }}>
        <ConnectorChips type="refutation" onSelect={w => setData({ ...data, fullEssayRefutation: (data.fullEssayRefutation || "") + w + " " })} />
        <TextArea value={data.fullEssayRefutation || ""}
          onChange={v => { setData({ ...data, fullEssayRefutation: v }); setFeedback(null); }}
          rows={4} label="🔄 הפרכה:" helperText="התייחסו לנימוק של הצד השני" />
      </div>

      <ConnectorChips type="summary" onSelect={w => setData({ ...data, fullEssaySummary: (data.fullEssaySummary || "") + w + " " })} />
      <TextArea value={data.fullEssaySummary || data.summary || ""}
        onChange={v => { setData({ ...data, fullEssaySummary: v }); setFeedback(null); }}
        rows={3} label="סיכום ומסקנה:" />

      {allFilled && (
        <Button onClick={getFb} variant="feedback" disabled={fbLoading}
          style={{ fontSize: 15, marginBottom: 8 }}>
          {fbLoading ? "בודק..." : "📝 בדקו את הטקסט המלא שלי"}
        </Button>
      )}
      <FeedbackBox feedback={feedback} loading={fbLoading} onRetry={getFb} />

      <div style={{ display: "flex", justifyContent: "space-between", marginTop: 20 }}>
        <Button onClick={onBack} variant="outline">→ חזרה</Button>
        <Button onClick={onNext} variant="success" disabled={!allFilled}>סיום – צפייה בטקסט המלא ←</Button>
      </div>
    </StageCard>
  );
}

function Stage10_FinalReview({ data, onBack, onPractice }) {
  const [feedback, setFeedback] = useState(null);
  const [fbLoading, setFbLoading] = useState(false);

  const getFb = async () => {
    const full = `פתיחה: ${data.fullEssayOpening}\n\nטענה: ${data.fullEssayClaim}\n\nנימוקים ודוגמאות: ${data.fullEssayArguments}\n\nהפרכה: ${data.fullEssayRefutation}\n\nסיכום: ${data.fullEssaySummary}`;
    setFbLoading(true);
    const fb = await getAIFeedback("full", full, data.topic?.title, data.fullEssayClaim, data.side);
    setFeedback(fb); setFbLoading(false);
  };

  return (
    <StageCard title="הטקסט הטיעוני המלא שלכם – עם הפרכה!" icon="🏆" color="#f9a825">
      <div style={{
        background: "linear-gradient(135deg, #fff9e8, #fff3d0)", borderRadius: 16,
        padding: "22px 26px", marginBottom: 22, border: "1px solid #ffe082", textAlign: "center",
      }}>
        <div style={{ fontSize: 44, marginBottom: 6 }}>🎉</div>
        <h3 style={{ fontSize: 20, color: "#f57f17", margin: "0 0 6px" }}>כל הכבוד! סיימתם!</h3>
        <p style={{ fontSize: 14, color: "#8a6a10", margin: 0 }}>כתבתם טקסט טיעוני מלא הכולל הפרכה!</p>
      </div>

      <div style={{
        background: "#fff", borderRadius: 16, padding: "24px 28px",
        border: "2px solid #f9a825", lineHeight: 2, fontSize: 15, color: "#2a1a4a",
        boxShadow: "0 4px 20px rgba(249,168,37,0.12)",
      }}>
        {[
          { label: "פתיחה", bg: "#e8f4ff", color: "#1565c0", text: data.fullEssayOpening },
          { label: "טענה", bg: "#f3e5f5", color: "#7b1fa2", text: data.fullEssayClaim },
          { label: "נימוקים ודוגמאות", bg: "#e0f2f1", color: "#00695c", text: data.fullEssayArguments },
          { label: "הפרכה", bg: "#ffebee", color: "#c62828", text: data.fullEssayRefutation },
          { label: "סיכום", bg: "#fff3e0", color: "#e65100", text: data.fullEssaySummary },
        ].map((s, i) => (
          <div key={i} style={{ marginBottom: 16 }}>
            <span style={{
              display: "inline-block", background: s.bg, color: s.color,
              padding: "2px 10px", borderRadius: 8, fontSize: 11, fontWeight: 700, marginBottom: 6,
            }}>{s.label}</span>
            <p style={{ margin: 0, whiteSpace: "pre-wrap" }}>{s.text}</p>
          </div>
        ))}
      </div>

      <div style={{ marginTop: 18, textAlign: "center" }}>
        <Button onClick={getFb} variant="feedback" disabled={fbLoading}
          style={{ fontSize: 14, padding: "14px 32px" }}>
          {fbLoading ? "🔍 בודק את הטקסט המלא..." : "📝 קבלו משוב סופי על הטקסט"}
        </Button>
      </div>
      <FeedbackBox feedback={feedback} loading={fbLoading} onRetry={getFb} />

      <div style={{ background: "#f5f0ff", borderRadius: 14, padding: "16px 20px", marginTop: 18, border: "1px solid #d0c4e8" }}>
        <h3 style={{ fontSize: 15, color: "#5a3e8e", margin: "0 0 8px" }}>🔍 רשימת בדיקה סופית</h3>
        {["הפתיחה מציגה את הנושא מבלי לחשוף את דעתי", "הטענה ברורה ומובנת",
          "יש לפחות 2 נימוקים עם דוגמאות", "ההפרכה מתייחסת לנימוק של הצד השני",
          "ההפרכה מסבירה למה הנימוק לא חזק דיו", "הסיכום חוזר על הטענה ומסיק מסקנה",
          "השתמשתי במילות קישור מתאימות"].map((item, i) => (
          <label key={i} style={{ display: "flex", alignItems: "center", gap: 8, marginBottom: 6, fontSize: 13, color: "#4a3a6a", cursor: "pointer" }}>
            <input type="checkbox" style={{ width: 16, height: 16, accentColor: "#6a4fa0" }} /> {item}
          </label>
        ))}
      </div>
      <div style={{ display: "flex", justifyContent: "space-between", marginTop: 20, flexWrap: "wrap", gap: 10 }}>
        <Button onClick={onBack} variant="outline">→ חזרה לעריכה</Button>
        <div style={{ display: "flex", gap: 10, flexWrap: "wrap" }}>
          <Button onClick={() => {
            const text = `${data.fullEssayOpening}\n\n${data.fullEssayClaim}\n\n${data.fullEssayArguments}\n\n${data.fullEssayRefutation}\n\n${data.fullEssaySummary}`;
            navigator.clipboard?.writeText(text).then(() => alert("✅ הטקסט הועתק בהצלחה!")).catch(() => {
              const ta = document.createElement("textarea"); ta.value = text; document.body.appendChild(ta); ta.select(); document.execCommand("copy"); document.body.removeChild(ta); alert("✅ הטקסט הועתק!");
            });
          }} variant="primary" style={{ background: "linear-gradient(135deg, #00897b, #4db6ac)" }}>📋 העתקה</Button>
          <Button onClick={() => window.print()} variant="secondary">🖨️ הדפסה</Button>
          <Button onClick={onPractice} variant="success">🔄 תרגול עם נושא חדש ←</Button>
        </div>
      </div>
    </StageCard>
  );
}

// ==================== PRACTICE MODE ====================

function PracticeMode({ onExit }) {
  const [topic, setTopic] = useState(null);
  const [customTopic, setCustomTopic] = useState("");
  const [pData, setPData] = useState({ opening: "", claim: "", side: null, arguments: "", refutation: "", summary: "" });
  const [feedback, setFeedback] = useState({});
  const [fbLoading, setFbLoading] = useState({});

  const topicTitle = topic?.id === "custom" ? customTopic : topic?.title;

  const getFb = async (section, content) => {
    setFbLoading(prev => ({ ...prev, [section]: true }));
    const fb = await getAIFeedback(
      section === "arguments" ? "arguments" : section === "full_review" ? "full" : section,
      content, topicTitle, pData.claim, pData.side
    );
    setFeedback(prev => ({ ...prev, [section]: fb }));
    setFbLoading(prev => ({ ...prev, [section]: false }));
  };

  if (!topic || (topic.id === "custom" && !customTopic.trim())) {
    return (
      <StageCard title="תרגול חופשי – בחרו נושא חדש" icon="🔄" color="#00897b">
        <InfoBox type="success">
          <strong>מצב תרגול!</strong> כאן אתם כותבים טקסט טיעוני מלא עם הפרכה – בלי הסברים, רק תרגול נטו. 💪
        </InfoBox>
        <div style={{ display: "grid", gap: 8 }}>
          {TOPICS.map(t => (
            <button key={t.id} onClick={() => {
              if (t.id === "custom") { setTopic(t); }
              else { setTopic(t); }
            }}
              style={{
                padding: "12px 16px", borderRadius: 12, textAlign: "right",
                border: topic?.id === t.id ? "2px solid #00897b" : "2px solid #e8e0f0",
                background: topic?.id === t.id ? "#e0f2f1" : "#faf8ff",
                cursor: "pointer", fontSize: 14, fontFamily: "'Heebo', sans-serif",
                color: t.id === "custom" ? "#e65100" : "#3d2a5c", transition: "all 0.2s",
                fontWeight: t.id === "custom" ? 700 : 400,
              }}>
              {t.id === "custom" ? "✨ " : ""}{t.title}
            </button>
          ))}
        </div>
        {topic?.id === "custom" && (
          <TextArea value={customTopic} onChange={setCustomTopic}
            placeholder="כתבו את הנושא שלכם..." rows={2} label="הנושא שלכם:" />
        )}
        <div style={{ display: "flex", justifyContent: "space-between", marginTop: 16 }}>
          <Button onClick={onExit} variant="outline">→ חזרה ללומדה</Button>
          {topic && topic.id !== "custom" && <Button onClick={() => {}}>נתחיל! ←</Button>}
          {topic?.id === "custom" && customTopic.trim() && <Button onClick={() => {}}>נתחיל! ←</Button>}
        </div>
      </StageCard>
    );
  }

  const allFilled = pData.opening?.trim() && pData.claim?.trim() && pData.arguments?.trim() && pData.refutation?.trim() && pData.summary?.trim();

  return (
    <>
      <StageCard title={`תרגול חופשי: ${topicTitle}`} icon="🔄" color="#00897b">
        <div style={{
          background: "#e0f2f1", borderRadius: 12, padding: "12px 16px", marginBottom: 16,
          border: "1px solid #a5d6a7", display: "flex", justifyContent: "space-between", alignItems: "center",
        }}>
          <span style={{ fontSize: 14, color: "#1b5e20", fontWeight: 600 }}>📝 הנושא: {topicTitle}</span>
          <div style={{ display: "flex", gap: 8 }}>
            <button onClick={() => { setTopic(null); setPData({ opening: "", claim: "", side: null, arguments: "", refutation: "", summary: "" }); setFeedback({}); }}
              style={{ background: "#fff", border: "1px solid #a5d6a7", borderRadius: 8, padding: "5px 14px", fontSize: 14, cursor: "pointer", fontFamily: "'Heebo', sans-serif", color: "#2e7d32" }}>
              החלף נושא
            </button>
            <button onClick={onExit}
              style={{ background: "#fff", border: "1px solid #c8c8c8", borderRadius: 8, padding: "5px 14px", fontSize: 14, cursor: "pointer", fontFamily: "'Heebo', sans-serif", color: "#666" }}>
              חזרה ללומדה
            </button>
          </div>
        </div>

        {/* Side selection */}
        <div style={{ display: "flex", gap: 12, marginBottom: 16 }}>
          {[["pro", "👍 בעד", "#43a047"], ["con", "👎 נגד", "#e53935"]].map(([side, label, color]) => (
            <button key={side} onClick={() => setPData({ ...pData, side })}
              style={{
                flex: 1, padding: "10px", borderRadius: 10, fontSize: 14, fontWeight: 700,
                fontFamily: "'Heebo', sans-serif", cursor: "pointer",
                background: pData.side === side ? color : "#f5f5f5",
                color: pData.side === side ? "#fff" : color,
                border: pData.side === side ? "none" : `2px solid ${color}40`, transition: "all 0.3s",
              }}>{label}</button>
          ))}
        </div>

        {/* Opening */}
        <TextArea value={pData.opening} onChange={v => { setPData({ ...pData, opening: v }); setFeedback(f => ({ ...f, opening: null })); }}
          rows={3} label="🚪 פתיחה:" helperText="הציגו את הנושא באופן כללי – בלי לחשוף דעה" />
        {pData.opening?.trim()?.length > 10 && (
          <Button onClick={() => getFb("opening", pData.opening)} variant="feedback" disabled={fbLoading.opening}
            style={{ fontSize: 15, marginBottom: 4 }}>{fbLoading.opening ? "..." : "📝 בדיקה"}</Button>
        )}
        <FeedbackBox feedback={feedback.opening} loading={fbLoading.opening} onRetry={() => getFb("opening", pData.opening)} />

        {/* Claim */}
        <TextArea value={pData.claim} onChange={v => { setPData({ ...pData, claim: v }); setFeedback(f => ({ ...f, claim: null })); }}
          rows={2} label="💪 טענה:" helperText="הביעו את דעתכם בבירור" />
        {pData.claim?.trim()?.length > 5 && (
          <Button onClick={() => getFb("claim", pData.claim)} variant="feedback" disabled={fbLoading.claim}
            style={{ fontSize: 15, marginBottom: 4 }}>{fbLoading.claim ? "..." : "📝 בדיקה"}</Button>
        )}
        <FeedbackBox feedback={feedback.claim} loading={fbLoading.claim} onRetry={() => getFb("claim", pData.claim)} />

        {/* Arguments */}
        <ConnectorChips type="beginning" onSelect={w => setPData({ ...pData, arguments: (pData.arguments || "") + w + " " })} />
        <ConnectorChips type="addition" onSelect={w => setPData({ ...pData, arguments: (pData.arguments || "") + w + " " })} />
        <TextArea value={pData.arguments} onChange={v => { setPData({ ...pData, arguments: v }); setFeedback(f => ({ ...f, arguments: null })); }}
          rows={6} label="📚 נימוקים ודוגמאות:" helperText="כתבו לפחות 2 נימוקים עם דוגמאות" />
        {pData.arguments?.trim()?.length > 20 && (
          <Button onClick={() => getFb("arguments", pData.arguments)} variant="feedback" disabled={fbLoading.arguments}
            style={{ fontSize: 15, marginBottom: 4 }}>{fbLoading.arguments ? "..." : "📝 בדיקה"}</Button>
        )}
        <FeedbackBox feedback={feedback.arguments} loading={fbLoading.arguments} onRetry={() => getFb("arguments", pData.arguments)} />

        {/* Refutation */}
        <div style={{ background: "#fff5f5", borderRadius: 14, padding: "14px 16px", marginBottom: 14, border: "1px solid #ffc8c8" }}>
          <ConnectorChips type="refutation" onSelect={w => setPData({ ...pData, refutation: (pData.refutation || "") + w + " " })} />
          <TextArea value={pData.refutation} onChange={v => { setPData({ ...pData, refutation: v }); setFeedback(f => ({ ...f, refutation: null })); }}
            rows={4} label="🔄 הפרכה:" helperText="התייחסו לנימוק של הצד השני והסבירו למה הוא לא חזק" />
        </div>
        {pData.refutation?.trim()?.length > 10 && (
          <Button onClick={() => getFb("refutation", pData.refutation)} variant="feedback" disabled={fbLoading.refutation}
            style={{ fontSize: 15, marginBottom: 4 }}>{fbLoading.refutation ? "..." : "📝 בדיקה"}</Button>
        )}
        <FeedbackBox feedback={feedback.refutation} loading={fbLoading.refutation} onRetry={() => getFb("refutation", pData.refutation)} />

        {/* Summary */}
        <ConnectorChips type="summary" onSelect={w => setPData({ ...pData, summary: (pData.summary || "") + w + " " })} />
        <TextArea value={pData.summary} onChange={v => { setPData({ ...pData, summary: v }); setFeedback(f => ({ ...f, summary: null })); }}
          rows={3} label="🎯 סיכום ומסקנה:" />
        {pData.summary?.trim()?.length > 10 && (
          <Button onClick={() => getFb("summary", pData.summary)} variant="feedback" disabled={fbLoading.summary}
            style={{ fontSize: 15, marginBottom: 4 }}>{fbLoading.summary ? "..." : "📝 בדיקה"}</Button>
        )}
        <FeedbackBox feedback={feedback.summary} loading={fbLoading.summary} onRetry={() => getFb("summary", pData.summary)} />

        {/* Full review */}
        {allFilled && (
          <div style={{ marginTop: 16, textAlign: "center" }}>
            <Button onClick={() => {
              const full = `פתיחה: ${pData.opening}\n\nטענה: ${pData.claim}\n\nנימוקים: ${pData.arguments}\n\nהפרכה: ${pData.refutation}\n\nסיכום: ${pData.summary}`;
              getFb("full_review", full);
            }} variant="success" disabled={fbLoading.full_review} style={{ fontSize: 14, padding: "14px 30px" }}>
              {fbLoading.full_review ? "בודק..." : "📝 משוב סופי על הטקסט המלא"}
            </Button>
            <FeedbackBox feedback={feedback.full_review} loading={fbLoading.full_review} onRetry={() => {
              const full = `פתיחה: ${pData.opening}\n\nטענה: ${pData.claim}\n\nנימוקים: ${pData.arguments}\n\nהפרכה: ${pData.refutation}\n\nסיכום: ${pData.summary}`;
              getFb("full_review", full);
            }} />
          </div>
        )}

        <div style={{ display: "flex", justifyContent: "space-between", marginTop: 20 }}>
          <Button onClick={onExit} variant="outline">→ חזרה ללומדה</Button>
          <div style={{ display: "flex", gap: 10 }}>
            <Button onClick={() => window.print()} variant="secondary">🖨️ הדפסה</Button>
            <Button onClick={() => { setTopic(null); setPData({ opening: "", claim: "", side: null, arguments: "", refutation: "", summary: "" }); setFeedback({}); }}
              variant="success">🔄 נושא חדש ←</Button>
          </div>
        </div>
      </StageCard>
    </>
  );
}

// ==================== CONFETTI ANIMATION ====================

function Confetti({ active }) {
  const [particles, setParticles] = useState([]);
  useEffect(() => {
    if (!active) { setParticles([]); return; }
    const colors = ["#ff6b6b", "#ffd93d", "#6bcb77", "#4d96ff", "#ff6eb4", "#a66cff", "#ff9f43"];
    const p = Array.from({ length: 60 }, (_, i) => ({
      id: i, x: Math.random() * 100, delay: Math.random() * 0.5,
      color: colors[Math.floor(Math.random() * colors.length)],
      size: 6 + Math.random() * 8, duration: 2 + Math.random() * 2,
      rotation: Math.random() * 360, type: Math.random() > 0.5 ? "circle" : "rect",
    }));
    setParticles(p);
    const t = setTimeout(() => setParticles([]), 4000);
    return () => clearTimeout(t);
  }, [active]);
  if (particles.length === 0) return null;
  return (
    <div style={{ position: "fixed", top: 0, left: 0, right: 0, bottom: 0, pointerEvents: "none", zIndex: 9999, overflow: "hidden" }}>
      {particles.map(p => (
        <div key={p.id} style={{
          position: "absolute", left: `${p.x}%`, top: "-10px",
          width: p.type === "circle" ? p.size : p.size * 0.7, height: p.size,
          background: p.color, borderRadius: p.type === "circle" ? "50%" : "2px",
          animation: `confettiFall ${p.duration}s ease-in ${p.delay}s forwards`,
          transform: `rotate(${p.rotation}deg)`,
        }} />
      ))}
      <style>{`
        @keyframes confettiFall {
          0% { transform: translateY(0) rotate(0deg); opacity: 1; }
          100% { transform: translateY(100vh) rotate(720deg); opacity: 0; }
        }
      `}</style>
    </div>
  );
}

// ==================== STAR BURST (quiz success) ====================

function StarBurst({ show }) {
  if (!show) return null;
  return (
    <div style={{ display: "inline-block", animation: "starPop 0.6s ease-out", fontSize: 28 }}>
      ⭐
      <style>{`
        @keyframes starPop {
          0% { transform: scale(0) rotate(-180deg); opacity: 0; }
          60% { transform: scale(1.4) rotate(20deg); opacity: 1; }
          100% { transform: scale(1) rotate(0deg); opacity: 1; }
        }
      `}</style>
    </div>
  );
}

// ==================== DAILY TIPS ====================

const DAILY_TIPS = [
  "💡 טיפ: פתיחה טובה לא חושפת דעה – היא מציגה דילמה!",
  "💡 טיפ: טענה חזקה מתחילה ב'לדעתי' ומביעה עמדה ברורה וחד-משמעית.",
  "💡 טיפ: נימוק טוב מתחיל במילת סדר (ראשית, שנית) ומסביר למה.",
  "💡 טיפ: דוגמה טובה מביאה הוכחה קונקרטית – ממחקר, מהניסיון, או מהחיים.",
  "💡 טיפ: בהפרכה, קודם מציגים את הצד השני ('אמנם...') ואז מפריכים ('אולם...').",
  "💡 טיפ: סיכום טוב חוזר על הטענה במילים אחרות ומסיים בהמלצה.",
  "💡 טיפ: מילות קישור הן הדבק של הטקסט – הן מחברות בין הרעיונות!",
  "💡 טיפ: הבדל בין הכללה לדוגמה: 'פגיעה בריכוז' = הכללה, 'חבר שלי לא מקשיב' = דוגמה.",
  "💡 טיפ: כל משפט חייב להסתיים בנקודה. בדקו לפני שממשיכים!",
  "💡 טיפ: אל תשכחו – בפתיחה מציגים שני צדדים, לא רק את הצד שלכם!",
];

// ==================== COLOR THEMES ====================

const THEMES = {
  purple: { name: "סגול", emoji: "💜", bg: "#f5f0ff", primary: "#6a4fa0", gradient: "linear-gradient(135deg, #5a3e8e, #8a65c8)", cardShadow: "rgba(90,62,142,0.07)", accent: "#9070c0" },
  blue: { name: "כחול", emoji: "💙", bg: "#f0f5ff", primary: "#1565c0", gradient: "linear-gradient(135deg, #0d47a1, #42a5f5)", cardShadow: "rgba(21,101,192,0.07)", accent: "#42a5f5" },
  green: { name: "ירוק", emoji: "💚", bg: "#f0fff5", primary: "#2e7d32", gradient: "linear-gradient(135deg, #1b5e20, #66bb6a)", cardShadow: "rgba(46,125,50,0.07)", accent: "#66bb6a" },
  pink: { name: "ורוד", emoji: "💗", bg: "#fff0f5", primary: "#c2185b", gradient: "linear-gradient(135deg, #880e4f, #f06292)", cardShadow: "rgba(194,24,91,0.07)", accent: "#f06292" },
};

// ==================== MAIN APP ====================

export default function App() {
  const [stage, setStage] = useState(0);
  const [practiceMode, setPracticeMode] = useState(false);
  const [data, setData] = useState({
    topic: null, customTopic: "", prosArguments: ["", "", ""], consArguments: ["", "", ""],
    opening: "", selectedOpeningStyle: undefined, selectedClaimStyle: undefined, side: null, claim: "",
    detailedArguments: null, summary: "", refutationPractice: {},
    fullEssayOpening: "", fullEssayClaim: "", fullEssayArguments: "",
    fullEssayRefutation: "", fullEssaySummary: "",
  });
  const [showJumpMenu, setShowJumpMenu] = useState(false);
  const [points, setPoints] = useState(0);
  const [completedStages, setCompletedStages] = useState(new Set());
  const [showConfetti, setShowConfetti] = useState(false);
  const [theme, setTheme] = useState("purple");
  const [showThemeMenu, setShowThemeMenu] = useState(false);
  const T = THEMES[theme];
  const dailyTip = useRef(DAILY_TIPS[Math.floor(Math.random() * DAILY_TIPS.length)]);

  const awardPoints = (stageNum, pts = 10) => {
    if (!completedStages.has(stageNum)) {
      setPoints(p => p + pts);
      setCompletedStages(s => new Set([...s, stageNum]));
    }
  };
  const triggerConfetti = () => { setShowConfetti(true); setTimeout(() => setShowConfetti(false), 100); };

  const scrollRef = useRef(null);
  useEffect(() => { scrollRef.current?.scrollTo({ top: 0, behavior: "smooth" }); }, [stage, practiceMode]);

  const P1 = ["בחירת נושא", "טיוטה", "פתיחה", "טענה", "נימוקים", "סיכום", "צפייה"];
  const P2 = ["לימוד הפרכה", "תרגול", "כתיבה מלאה", "סיום"];
  const ALL_STAGES = [...P1, ...P2];
  const next = () => { awardPoints(stage); if (stage === 5 || stage === 10) triggerConfetti(); setStage(s => Math.min(s + 1, 10)); };
  const back = () => setStage(s => Math.max(s - 1, 0));
  const goTo = (s) => { setStage(s); setShowJumpMenu(false); };
  const isPart2 = stage >= 7;

  const handleReset = () => {
    if (confirm("האם אתם בטוחים? כל ההתקדמות תימחק!")) {
      setStage(0);
      setData({
        topic: null, customTopic: "", prosArguments: ["", "", ""], consArguments: ["", "", ""],
        opening: "", selectedOpeningStyle: undefined, selectedClaimStyle: undefined, side: null, claim: "",
        detailedArguments: null, summary: "", refutationPractice: {},
        fullEssayOpening: "", fullEssayClaim: "", fullEssayArguments: "",
        fullEssayRefutation: "", fullEssaySummary: "",
      });
    }
  };

  const stages = [
    <Stage0_TopicSelect data={data} setData={setData} onNext={next} />,
    <Stage1_Draft data={data} setData={setData} onNext={next} onBack={back} />,
    <Stage2_Opening data={data} setData={setData} onNext={next} onBack={back} />,
    <Stage3_Claim data={data} setData={setData} onNext={next} onBack={back} />,
    <Stage4_Arguments data={data} setData={setData} onNext={next} onBack={back} />,
    <Stage5_Summary data={data} setData={setData} onNext={next} onBack={back} />,
    <Stage6_Review data={data} onNext={next} onBack={back} />,
    <Stage7_LearnRefutation data={data} onNext={next} onBack={back} />,
    <Stage8_PracticeRefutation data={data} setData={setData} onNext={next} onBack={back} />,
    <Stage9_FullEssay data={data} setData={setData} onNext={next} onBack={back} />,
    <Stage10_FinalReview data={data} onBack={back} onPractice={() => setPracticeMode(true)} />,
  ];

  return (
    <div ref={scrollRef} style={{
      minHeight: "100vh", direction: "rtl",
      background: `linear-gradient(180deg, ${T.bg} 0%, ${T.bg}ee 30%, ${T.bg} 100%)`,
      backgroundImage: `linear-gradient(180deg, ${T.bg} 0%, ${T.bg}ee 30%, ${T.bg} 100%), radial-gradient(circle at 20% 50%, ${T.primary}08 0%, transparent 50%), radial-gradient(circle at 80% 20%, ${T.accent}08 0%, transparent 50%)`,
      fontFamily: "'Heebo', sans-serif",
    }}>
      <Confetti active={showConfetti} />
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Heebo:wght@300;400;500;600;700;800;900&display=swap');
        @keyframes fadeSlideIn { from { opacity: 0; transform: translateY(14px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes pulse { 0%,100% { opacity: 1; } 50% { opacity: 0.5; } }
        @keyframes bounce { 0%,100% { transform: translateY(0); } 50% { transform: translateY(-4px); } }
        @keyframes iconFloat { 0%,100% { transform: translateY(0) rotate(0deg); } 50% { transform: translateY(-3px) rotate(5deg); } }
        * { box-sizing: border-box; }
        @media (max-width: 768px) {
          .main-container { padding: 16px 14px 50px !important; }
        }
        @media print { body { direction: rtl; } }
      `}</style>

      <div className="main-container" style={{ maxWidth: 960, margin: "0 auto", padding: "24px 24px 60px" }}>
        {/* Header */}
        <div style={{ textAlign: "center", marginBottom: 16, animation: "fadeSlideIn 0.6s ease-out" }}>
          <h1 style={{
            fontSize: 36, fontWeight: 900, margin: "0 0 6px",
            background: T.gradient,
            WebkitBackgroundClip: "text", WebkitTextFillColor: "transparent",
          }}>✏️ לומדת כתיבה טיעונית</h1>
          <p style={{ fontSize: 18, color: T.primary + "99", margin: 0 }}>
            {practiceMode ? "מצב תרגול חופשי 🔄" : "שיטת פטנד\"ס – פתיחה · טענה · נימוקים · דוגמאות · סיכום"}
          </p>
          <p style={{ fontSize: 15, color: T.primary, margin: "8px 0 0", fontWeight: 700 }}>
            יצרה וערכה בעזרת בינה מלאכותית: מורן קמיל גלברג – הוראה מותאמת
          </p>
        </div>

        {/* Points + Theme bar */}
        <div style={{
          display: "flex", justifyContent: "space-between", alignItems: "center",
          marginBottom: 14, padding: "8px 16px", background: "#fff", borderRadius: 14,
          boxShadow: `0 2px 12px ${T.cardShadow}`, border: `1px solid ${T.primary}15`,
        }}>
          {/* Points */}
          <div style={{ display: "flex", alignItems: "center", gap: 8 }}>
            <span style={{ fontSize: 22, animation: "bounce 2s infinite" }}>⭐</span>
            <span style={{ fontSize: 18, fontWeight: 800, color: T.primary }}>{points}</span>
            <span style={{ fontSize: 14, color: T.primary + "88" }}>נקודות</span>
          </div>
          {/* Stars for completed stages */}
          <div style={{ display: "flex", gap: 3 }}>
            {Array.from({ length: 11 }, (_, i) => (
              <span key={i} style={{
                fontSize: 16, opacity: completedStages.has(i) ? 1 : 0.2,
                transition: "all 0.3s",
                transform: completedStages.has(i) ? "scale(1)" : "scale(0.8)",
              }}>{completedStages.has(i) ? "🌟" : "☆"}</span>
            ))}
          </div>
          {/* Theme picker */}
          <div style={{ position: "relative" }}>
            <button onClick={() => setShowThemeMenu(!showThemeMenu)} style={{
              background: T.gradient, border: "none", borderRadius: 10, padding: "6px 14px",
              fontSize: 14, cursor: "pointer", fontFamily: "'Heebo', sans-serif", color: "#fff",
              fontWeight: 600, display: "flex", alignItems: "center", gap: 4,
            }}>🎨 ערכת צבעים</button>
            {showThemeMenu && (
              <div style={{
                position: "absolute", top: "100%", left: 0, marginTop: 4, background: "#fff",
                borderRadius: 12, boxShadow: "0 8px 24px rgba(0,0,0,0.15)", padding: 8, zIndex: 100,
                display: "flex", gap: 6, border: "1px solid #e0e0e0",
              }}>
                {Object.entries(THEMES).map(([key, t]) => (
                  <button key={key} onClick={() => { setTheme(key); setShowThemeMenu(false); }}
                    style={{
                      padding: "8px 14px", borderRadius: 10, border: theme === key ? `2px solid ${t.primary}` : "1px solid #eee",
                      background: theme === key ? t.bg : "#fff", cursor: "pointer",
                      fontFamily: "'Heebo', sans-serif", fontSize: 14, fontWeight: 600,
                      color: t.primary, display: "flex", alignItems: "center", gap: 4,
                    }}>{t.emoji} {t.name}</button>
                ))}
              </div>
            )}
          </div>
        </div>

        {/* Daily tip */}
        {stage === 0 && !practiceMode && (
          <div style={{
            background: `linear-gradient(135deg, ${T.primary}10, ${T.accent}10)`,
            border: `1px solid ${T.primary}25`, borderRadius: 14, padding: "12px 18px",
            marginBottom: 16, fontSize: 16, color: T.primary, lineHeight: 1.7,
            animation: "fadeSlideIn 1s ease-out",
          }}>
            {dailyTip.current}
          </div>
        )}

        {/* Progress bar with percentage */}
        {!practiceMode && stage > 0 && (
          <div style={{ marginBottom: 16 }}>
            <div style={{
              display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 6,
            }}>
              <span style={{ fontSize: 14, fontWeight: 700, color: T.primary }}>
                {isPart2 ? "חלק ב' – הפרכה" : "חלק א' – כתיבה טיעונית"}
              </span>
              <span style={{ fontSize: 16, fontWeight: 800, color: T.primary }}>
                {Math.round(((stage) / 10) * 100)}%
              </span>
            </div>
            <div style={{
              height: 10, background: T.primary + "20", borderRadius: 10, overflow: "hidden",
            }}>
              <div style={{
                height: "100%", borderRadius: 10,
                background: T.gradient, transition: "width 0.6s ease",
                width: `${((stage) / 10) * 100}%`,
              }} />
            </div>
          </div>
        )}

        {/* Stage navigation toolbar */}
        {!practiceMode && (
          <div style={{
            display: "flex", justifyContent: "center", gap: 8, marginBottom: 12, position: "relative",
          }}>
            <button onClick={() => setShowJumpMenu(!showJumpMenu)} style={{
              background: "#fff", border: "1px solid #d0c4e8", borderRadius: 10, padding: "6px 14px",
              fontSize: 12, cursor: "pointer", fontFamily: "'Heebo', sans-serif", color: "#6a4fa0",
              fontWeight: 600, display: "flex", alignItems: "center", gap: 4,
            }}>
              📍 קפיצה לשלב
            </button>
            <button onClick={handleReset} style={{
              background: "#fff", border: "1px solid #ffccbc", borderRadius: 10, padding: "6px 14px",
              fontSize: 12, cursor: "pointer", fontFamily: "'Heebo', sans-serif", color: "#c62828",
              fontWeight: 600,
            }}>
              🗑️ התחל מחדש
            </button>

            {showJumpMenu && (
              <div style={{
                position: "absolute", top: 40, background: "#fff", borderRadius: 14, padding: "12px 16px",
                boxShadow: "0 8px 32px rgba(90,62,142,0.15)", border: "1px solid #e0d6f0",
                zIndex: 100, minWidth: 260,
              }}>
                <p style={{ fontSize: 13, color: "#5a3e8e", margin: "0 0 10px", fontWeight: 700 }}>📍 בחרו שלב:</p>
                <div style={{ display: "flex", flexDirection: "column", gap: 4 }}>
                  <p style={{ fontSize: 11, color: "#9a8cb8", margin: "0 0 4px", fontWeight: 600 }}>חלק א' – כתיבה טיעונית:</p>
                  {P1.map((name, i) => (
                    <button key={i} onClick={() => goTo(i)} style={{
                      padding: "8px 14px", borderRadius: 8, textAlign: "right", fontSize: 15,
                      fontFamily: "'Heebo', sans-serif", cursor: "pointer", border: "none",
                      background: stage === i ? "linear-gradient(135deg, #6a4fa0, #9a75d6)" : "#f5f0ff",
                      color: stage === i ? "#fff" : "#5a3e8e", fontWeight: stage === i ? 700 : 400,
                      transition: "all 0.2s",
                    }}>
                      {i < stage ? "✓ " : `${i + 1}. `}{name}
                    </button>
                  ))}
                  <p style={{ fontSize: 11, color: "#c0a0a0", margin: "8px 0 4px", fontWeight: 600 }}>חלק ב' – הפרכה:</p>
                  {P2.map((name, i) => (
                    <button key={i + 7} onClick={() => goTo(i + 7)} style={{
                      padding: "8px 14px", borderRadius: 8, textAlign: "right", fontSize: 15,
                      fontFamily: "'Heebo', sans-serif", cursor: "pointer", border: "none",
                      background: stage === i + 7 ? "linear-gradient(135deg, #c62828, #ef5350)" : "#fef0f0",
                      color: stage === i + 7 ? "#fff" : "#c62828", fontWeight: stage === i + 7 ? 700 : 400,
                      transition: "all 0.2s",
                    }}>
                      {i + 7 < stage ? "✓ " : `${i + 1}. `}{name}
                    </button>
                  ))}
                </div>
                <button onClick={() => setShowJumpMenu(false)} style={{
                  width: "100%", marginTop: 10, padding: "6px", borderRadius: 8, border: "1px solid #e0d6f0",
                  background: "#faf8ff", fontSize: 14, cursor: "pointer", fontFamily: "'Heebo', sans-serif",
                  color: "#8a7aaa",
                }}>סגור ✕</button>
              </div>
            )}
          </div>
        )}

        {practiceMode ? (
          <PracticeMode onExit={() => setPracticeMode(false)} />
        ) : (
          <>
            <div style={{ display: "flex", gap: 10, justifyContent: "center", marginBottom: 16 }}>
              {[["חלק א' – כתיבה טיעונית", !isPart2, "#6a4fa0", "#9070c0"],
                ["חלק ב' – הפרכה", isPart2, "#c62828", "#ef5350"]].map(([text, active, c1, c2], i) => (
                <div key={i} onClick={() => goTo(i === 0 ? Math.min(stage, 6) : Math.max(stage, 7))} style={{
                  padding: "7px 20px", borderRadius: 28, fontSize: 13, fontWeight: 700, cursor: "pointer",
                  background: active ? `linear-gradient(135deg, ${c1}, ${c2})` : i === 0 ? "#e8e0f0" : "#f0e0e0",
                  color: active ? "#fff" : i === 0 ? "#9a8cb8" : "#c0a0a0",
                  boxShadow: active ? `0 3px 12px ${c1}40` : "none", transition: "all 0.4s",
                }}>{text}</div>
              ))}
            </div>

            {!isPart2 ? <ProgressBar currentStep={stage} totalSteps={7} stepNames={P1} onStepClick={(i) => goTo(i)} />
              : <ProgressBar currentStep={stage - 7} totalSteps={4} stepNames={P2} onStepClick={(i) => goTo(i + 7)} />}

            {stages[stage]}
          </>
        )}
      </div>
    </div>
  );
}
