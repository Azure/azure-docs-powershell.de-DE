---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B0AE1969-71FD-4B6E-B0C0-1B744814BD5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93dc73193c300f0f10fd9dccaff1c1f3954b8306
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006238"
---
# <span data-ttu-id="4c539-101">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c539-101">Start-AzureAutomationRunbook</span></span>

## <span data-ttu-id="4c539-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c539-102">SYNOPSIS</span></span>

<span data-ttu-id="4c539-103">Startet einen runbooks-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="4c539-103">Starts a runbook job.</span></span>

## <span data-ttu-id="4c539-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c539-104">SYNTAX</span></span>

```
Start-AzureAutomationRunbook -Name <String> [-Parameters <IDictionary>] [-RunOn <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4c539-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c539-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4c539-106">Mit dem Cmdlet **Start-AzureAutomationRunbook** wird ein Microsoft Azure Automation runbooks-Auftrag gestartet.</span><span class="sxs-lookup"><span data-stu-id="4c539-106">The **Start-AzureAutomationRunbook** cmdlet starts a Microsoft Azure Automation runbook job.</span></span>
<span data-ttu-id="4c539-107">Geben Sie die ID oder den Namen eines runbooks an.</span><span class="sxs-lookup"><span data-stu-id="4c539-107">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="4c539-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c539-108">EXAMPLES</span></span>

### <span data-ttu-id="4c539-109">Beispiel 1: Starten eines runbooks-Auftrags</span><span class="sxs-lookup"><span data-stu-id="4c539-109">Example 1: Start a runbook job</span></span>
```
PS C:\> Start-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="4c539-110">Dieser Befehl startet einen runbooks-Auftrag für den runbooks mit dem Namen Runbk01 im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4c539-110">This command starts a runbook job for the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4c539-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c539-111">PARAMETERS</span></span>

### <span data-ttu-id="4c539-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4c539-112">-AutomationAccountName</span></span>
<span data-ttu-id="4c539-113">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4c539-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="4c539-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4c539-114">-Name</span></span>
<span data-ttu-id="4c539-115">Gibt den Namen einer runbooks an.</span><span class="sxs-lookup"><span data-stu-id="4c539-115">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="4c539-116">-Parameter</span><span class="sxs-lookup"><span data-stu-id="4c539-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c539-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="4c539-117">-Profile</span></span>
<span data-ttu-id="4c539-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4c539-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c539-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4c539-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4c539-120">-RunOn</span><span class="sxs-lookup"><span data-stu-id="4c539-120">-RunOn</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c539-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c539-121">CommonParameters</span></span>
<span data-ttu-id="4c539-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c539-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c539-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c539-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c539-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c539-124">INPUTS</span></span>

## <span data-ttu-id="4c539-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c539-125">OUTPUTS</span></span>

### <span data-ttu-id="4c539-126">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="4c539-126">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="4c539-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c539-127">NOTES</span></span>

## <span data-ttu-id="4c539-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c539-128">RELATED LINKS</span></span>

[<span data-ttu-id="4c539-129">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c539-129">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="4c539-130">Neu – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c539-130">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="4c539-131">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c539-131">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="4c539-132">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c539-132">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="4c539-133">Satz-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c539-133">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)


