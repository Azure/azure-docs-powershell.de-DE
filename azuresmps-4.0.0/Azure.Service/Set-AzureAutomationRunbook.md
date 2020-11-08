---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C24CFC83-3151-452D-A7B9-E78466493474
online version: ''
schema: 2.0.0
ms.openlocfilehash: e193dba6f64553e5e52d7f900bdc5c54deac5112
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006278"
---
# <span data-ttu-id="7c7c7-101">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c7c7-101">Set-AzureAutomationRunbook</span></span>

## <span data-ttu-id="7c7c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c7c7-102">SYNOPSIS</span></span>

<span data-ttu-id="7c7c7-103">Ändert die Konfiguration eines runbooks.</span><span class="sxs-lookup"><span data-stu-id="7c7c7-103">Modifies the configuration of a runbook.</span></span>

## <span data-ttu-id="7c7c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c7c7-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7c7c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c7c7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7c7c7-106">Das Cmdlet " **Satz-AzureAutomationRunbook** " ändert die Konfiguration eines Microsoft Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="7c7c7-106">The **Set-AzureAutomationRunbook** cmdlet modifies the configuration of a Microsoft Azure Automation runbook.</span></span>

## <span data-ttu-id="7c7c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c7c7-107">EXAMPLES</span></span>

### <span data-ttu-id="7c7c7-108">Beispiel 1: Aktivieren der ausführlichen Protokollierung für ein runbooks</span><span class="sxs-lookup"><span data-stu-id="7c7c7-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook" -LogVerbose $True
```

<span data-ttu-id="7c7c7-109">Dieser Befehl aktiviert die ausführliche Protokollierung für die Aufträge des angegebenen runbooks im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7c7c7-109">This command enables verbose logging for the jobs of the specified runbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7c7c7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c7c7-110">PARAMETERS</span></span>

### <span data-ttu-id="7c7c7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7c7c7-111">-AutomationAccountName</span></span>
<span data-ttu-id="7c7c7-112">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="7c7c7-112">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c7-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c7c7-113">-Description</span></span>
<span data-ttu-id="7c7c7-114">Gibt eine Beschreibung für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="7c7c7-114">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c7-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="7c7c7-115">-LogProgress</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c7-116">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="7c7c7-116">-LogVerbose</span></span>
<span data-ttu-id="7c7c7-117">Gibt an, ob die ausführliche Protokollierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c7c7-117">Indicates whether to use verbose logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7c7c7-118">-Name</span></span>
<span data-ttu-id="7c7c7-119">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="7c7c7-119">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c7-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="7c7c7-120">-Profile</span></span>
<span data-ttu-id="7c7c7-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7c7c7-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7c7c7-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7c7c7-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c7-123">-Tags</span><span class="sxs-lookup"><span data-stu-id="7c7c7-123">-Tags</span></span>
<span data-ttu-id="7c7c7-124">Gibt ein Array von Tags an.</span><span class="sxs-lookup"><span data-stu-id="7c7c7-124">Specifies an array of tags.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7c7-125">CommonParameters</span></span>
<span data-ttu-id="7c7c7-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c7c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7c7-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c7c7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7c7-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c7c7-128">INPUTS</span></span>

## <span data-ttu-id="7c7c7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c7c7-129">OUTPUTS</span></span>

### <span data-ttu-id="7c7c7-130">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="7c7c7-130">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="7c7c7-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c7c7-131">NOTES</span></span>

## <span data-ttu-id="7c7c7-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c7c7-132">RELATED LINKS</span></span>

[<span data-ttu-id="7c7c7-133">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c7c7-133">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="7c7c7-134">Neu – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c7c7-134">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="7c7c7-135">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c7c7-135">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="7c7c7-136">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c7c7-136">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="7c7c7-137">Anfang-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c7c7-137">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


