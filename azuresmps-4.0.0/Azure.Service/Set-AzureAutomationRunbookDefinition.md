---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C583BECF-7FC2-4A1F-9788-5CB19E73956C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9464e811597ba0fe5bfe2d53643c7b788c9be71e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006276"
---
# <span data-ttu-id="b6e99-101">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="b6e99-101">Set-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="b6e99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6e99-102">SYNOPSIS</span></span>

<span data-ttu-id="b6e99-103">Aktualisiert die Entwurfsdefinition eines runbooks.</span><span class="sxs-lookup"><span data-stu-id="b6e99-103">Updates the draft definition of a runbook.</span></span>

## <span data-ttu-id="b6e99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6e99-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbookDefinition -Name <String> -Path <String> [-Overwrite] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b6e99-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6e99-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b6e99-106">Das Cmdlet " **Satz-AzureAutomationRunbookDefinition** " aktualisiert die Entwurfsdefinition eines Microsoft Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="b6e99-106">The **Set-AzureAutomationRunbookDefinition** cmdlet updates the draft definition of a Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="b6e99-107">Geben Sie eine Windows PowerShell-Skriptdatei (. ps1) an, die einen runbooks enthält, der zum Entwurfs runbooks wird.</span><span class="sxs-lookup"><span data-stu-id="b6e99-107">Specify a Windows PowerShell script (.ps1) file that contains a runbook that becomes the draft runbook.</span></span>

<span data-ttu-id="b6e99-108">Wenn bereits eine Entwurfsdefinition vorhanden ist, verwenden Sie den Parameter *overwrite* , um das Cmdlet zu zwingen, den vorhandenen Entwurf zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="b6e99-108">If a draft definition already exists, use the *Overwrite* parameter to force the cmdlet to overwrite the existing draft.</span></span>

## <span data-ttu-id="b6e99-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6e99-109">EXAMPLES</span></span>

### <span data-ttu-id="b6e99-110">Beispiel 1: Überschreiben einer vorhandenen Entwurfsdefinition eines runbooks</span><span class="sxs-lookup"><span data-stu-id="b6e99-110">Example 1: Overwrite an existing draft definition of a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "Runbk01" -Path ".\App01.ps1" -Overwrite
```

<span data-ttu-id="b6e99-111">Mit diesem Befehl wird die vorhandene Entwurfsdefinition eines runbooks überschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6e99-111">This command overwrites the existing draft definition of a runbook.</span></span>

## <span data-ttu-id="b6e99-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6e99-112">PARAMETERS</span></span>

### <span data-ttu-id="b6e99-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b6e99-113">-AutomationAccountName</span></span>
<span data-ttu-id="b6e99-114">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b6e99-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="b6e99-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b6e99-115">-Name</span></span>
<span data-ttu-id="b6e99-116">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="b6e99-116">Specifies a name.</span></span>

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

### <span data-ttu-id="b6e99-117">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="b6e99-117">-Overwrite</span></span>
<span data-ttu-id="b6e99-118">Gibt an, ob eine vorhandene Entwurfsdefinition überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6e99-118">Indicates whether to overwrite an existing draft definition.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e99-119">-Path</span><span class="sxs-lookup"><span data-stu-id="b6e99-119">-Path</span></span>
<span data-ttu-id="b6e99-120">Gibt den Pfad zu einer runbooks an.</span><span class="sxs-lookup"><span data-stu-id="b6e99-120">Specifies the path to a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e99-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="b6e99-121">-Profile</span></span>
<span data-ttu-id="b6e99-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b6e99-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6e99-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b6e99-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6e99-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e99-124">CommonParameters</span></span>
<span data-ttu-id="b6e99-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6e99-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e99-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6e99-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e99-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6e99-127">INPUTS</span></span>

## <span data-ttu-id="b6e99-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6e99-128">OUTPUTS</span></span>

### <span data-ttu-id="b6e99-129">Microsoft. Azure. Commands. Automation. Model. RunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="b6e99-129">Microsoft.Azure.Commands.Automation.Model.RunbookDefinition</span></span>

## <span data-ttu-id="b6e99-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6e99-130">NOTES</span></span>

## <span data-ttu-id="b6e99-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6e99-131">RELATED LINKS</span></span>

[<span data-ttu-id="b6e99-132">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="b6e99-132">Get-AzureAutomationRunbookDefinition</span></span>](./Get-AzureAutomationRunbookDefinition.md)


