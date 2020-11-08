---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 304F71E0-9E89-46E6-BD25-7584601CC845
online version: ''
schema: 2.0.0
ms.openlocfilehash: e507b1b35bf8739c80bbdf92f02f29099ceb3284
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005863"
---
# <span data-ttu-id="a8633-101">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8633-101">Get-AzureAutomationRunbook</span></span>

## <span data-ttu-id="a8633-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8633-102">SYNOPSIS</span></span>

<span data-ttu-id="a8633-103">Ruft einen runbooks ab.</span><span class="sxs-lookup"><span data-stu-id="a8633-103">Gets a runbook.</span></span>

## <span data-ttu-id="a8633-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8633-104">SYNTAX</span></span>

### <span data-ttu-id="a8633-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8633-105">ByAll (Default)</span></span>
```
Get-AzureAutomationRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a8633-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="a8633-106">ByRunbookName</span></span>
```
Get-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8633-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8633-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a8633-108">Das Cmdlet " **Get-AzureAutomationRunbook** " ruft mindestens ein Microsoft Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="a8633-108">The **Get-AzureAutomationRunbook** cmdlet gets one or more Microsoft Azure Automation runbooks.</span></span>
<span data-ttu-id="a8633-109">Standardmäßig werden alle runbooks zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8633-109">By default, all runbooks are returned.</span></span>
<span data-ttu-id="a8633-110">Um eine bestimmte runbooks zu erhalten, geben Sie den Namen oder die ID an.</span><span class="sxs-lookup"><span data-stu-id="a8633-110">To get a specific runbook, specify its name or ID.</span></span>
<span data-ttu-id="a8633-111">Wenn Sie alle runbooks mit einem bestimmten Zeitplan verknüpfen möchten, geben Sie den Namen des Zeitplans an.</span><span class="sxs-lookup"><span data-stu-id="a8633-111">To get all runbooks linked to a specific schedule, specify the schedule name.</span></span>

## <span data-ttu-id="a8633-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8633-112">EXAMPLES</span></span>

### <span data-ttu-id="a8633-113">Beispiel 1: Abrufen aller runbooks</span><span class="sxs-lookup"><span data-stu-id="a8633-113">Example 1: Get all runbooks</span></span>
```
PS C:\> Get-AzureAutomationRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="a8633-114">Dieser Befehl ruft alle runbooks im Azure Automation-Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="a8633-114">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a8633-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8633-115">PARAMETERS</span></span>

### <span data-ttu-id="a8633-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a8633-116">-AutomationAccountName</span></span>
<span data-ttu-id="a8633-117">Gibt den Namen eines Azure Automation-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a8633-117">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="a8633-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a8633-118">-Name</span></span>
<span data-ttu-id="a8633-119">Gibt den Namen einer runbooks an.</span><span class="sxs-lookup"><span data-stu-id="a8633-119">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8633-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="a8633-120">-Profile</span></span>
<span data-ttu-id="a8633-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a8633-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8633-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a8633-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a8633-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8633-123">CommonParameters</span></span>
<span data-ttu-id="a8633-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8633-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8633-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8633-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8633-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8633-126">INPUTS</span></span>

## <span data-ttu-id="a8633-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8633-127">OUTPUTS</span></span>

### <span data-ttu-id="a8633-128">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="a8633-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="a8633-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8633-129">NOTES</span></span>

## <span data-ttu-id="a8633-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8633-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8633-131">Neu – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8633-131">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="a8633-132">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8633-132">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="a8633-133">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8633-133">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="a8633-134">Satz-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8633-134">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="a8633-135">Anfang-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8633-135">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


