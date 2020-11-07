---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: f71aef989a26ec5998ee8fd059446a2b05c2e4b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665319"
---
# <span data-ttu-id="ae6bd-101">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="ae6bd-101">Get-AzureRmAutomationDscNodeReport</span></span>

## <span data-ttu-id="ae6bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6bd-103">Ruft Berichte ab, die von einem DSC-Knoten an die Automatisierung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-103">Gets reports sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae6bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae6bd-104">SYNTAX</span></span>

### <span data-ttu-id="ae6bd-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="ae6bd-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae6bd-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="ae6bd-106">ByLatest</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae6bd-107">ById</span><span class="sxs-lookup"><span data-stu-id="ae6bd-107">ById</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae6bd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae6bd-108">DESCRIPTION</span></span>
<span data-ttu-id="ae6bd-109">Das Cmdlet " **Get-AzureRmAutomationDscNodeReport** " ruft Berichte ab, die von einem APS-Knoten (Desired State Configuration, DSC) an Azure Automation gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-109">The **Get-AzureRmAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="ae6bd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae6bd-110">EXAMPLES</span></span>

### <span data-ttu-id="ae6bd-111">Beispiel 1: Abrufen aller Berichte für einen DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="ae6bd-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="ae6bd-112">Der erste Befehl ruft den DSC-Knoten für den Computer mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="ae6bd-113">Der Befehl speichert dieses Objekt in der $Node-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-113">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="ae6bd-114">Der zweite Befehl ruft Metadaten für alle Berichte ab, die vom DSC-Knoten mit dem Namen Computer14 an das Automatisierungs Konto mit dem Namen Contoso17 gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="ae6bd-115">Der Befehl gibt den Knoten mithilfe der **ID** -Eigenschaft des $Node-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="ae6bd-116">Beispiel 2: Abrufen eines Berichts für einen DSC-Knoten nach Berichts-ID</span><span class="sxs-lookup"><span data-stu-id="ae6bd-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="ae6bd-117">Der erste Befehl ruft den DSC-Knoten für den Computer mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="ae6bd-118">Der Befehl speichert dieses Objekt in der $Node-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-118">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="ae6bd-119">Der zweite Befehl ruft Metadaten für den Bericht ab, der durch die angegebene ID identifiziert wird, die vom DSC-Knoten mit dem Namen Computer14 an das Automatisierungs Konto mit dem Namen Contoso17 gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="ae6bd-120">Beispiel 3: Abrufen des neuesten Berichts für einen DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="ae6bd-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="ae6bd-121">Der erste Befehl ruft den DSC-Knoten für den Computer mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="ae6bd-122">Der Befehl speichert dieses Objekt in der $Node-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-122">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="ae6bd-123">Der zweite Befehl ruft Metadaten für den neuesten Bericht ab, der vom DSC-Knoten mit dem Namen Computer14 an das Automatisierungs Konto mit dem Namen Contoso17 gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ae6bd-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae6bd-124">PARAMETERS</span></span>

### <span data-ttu-id="ae6bd-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ae6bd-125">-AutomationAccountName</span></span>
<span data-ttu-id="ae6bd-126">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="ae6bd-127">Dieses Cmdlet exportiert Berichte für einen DSC-Knoten, der zu dem Konto gehört, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6bd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6bd-128">-DefaultProfile</span></span>
<span data-ttu-id="ae6bd-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ae6bd-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae6bd-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ae6bd-130">-EndTime</span></span>
<span data-ttu-id="ae6bd-131">Gibt eine Endzeit an.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-131">Specifies an end time.</span></span>
<span data-ttu-id="ae6bd-132">Dieses Cmdlet ruft Berichte ab, die von der Automatisierung vor diesem Zeitpunkt empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6bd-133">-ID</span><span class="sxs-lookup"><span data-stu-id="ae6bd-133">-Id</span></span>
<span data-ttu-id="ae6bd-134">Gibt die eindeutige ID des DSC-Knoten Berichts an, der für dieses Cmdlet abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6bd-135">-Neueste</span><span class="sxs-lookup"><span data-stu-id="ae6bd-135">-Latest</span></span>
<span data-ttu-id="ae6bd-136">Gibt an, dass dieses Cmdlet nur den neuesten DSC-Bericht für den angegebenen Knoten abruft.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByLatest
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae6bd-137">-Knoten-Nr</span><span class="sxs-lookup"><span data-stu-id="ae6bd-137">-NodeId</span></span>
<span data-ttu-id="ae6bd-138">Gibt die eindeutige ID des DSC-Knotens an, für den dieses Cmdlet Berichte abruft.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6bd-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae6bd-139">-ResourceGroupName</span></span>
<span data-ttu-id="ae6bd-140">Gibt den Namen einer Ressourcengruppe an, die den DSC-Knoten enthält, für den dieses Cmdlet Berichte abruft.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6bd-141">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="ae6bd-141">-StartTime</span></span>
<span data-ttu-id="ae6bd-142">Gibt eine Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-142">Specifies a start time.</span></span>
<span data-ttu-id="ae6bd-143">Dieses Cmdlet ruft Berichte ab, die von der Automatisierung nach diesem Zeitpunkt empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6bd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6bd-144">CommonParameters</span></span>
<span data-ttu-id="ae6bd-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6bd-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae6bd-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6bd-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae6bd-147">INPUTS</span></span>

### <span data-ttu-id="ae6bd-148">Keine</span><span class="sxs-lookup"><span data-stu-id="ae6bd-148">None</span></span>
<span data-ttu-id="ae6bd-149">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ae6bd-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae6bd-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae6bd-150">OUTPUTS</span></span>

### <span data-ttu-id="ae6bd-151">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="ae6bd-151">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="ae6bd-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae6bd-152">NOTES</span></span>

## <span data-ttu-id="ae6bd-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae6bd-153">RELATED LINKS</span></span>

[<span data-ttu-id="ae6bd-154">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ae6bd-154">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="ae6bd-155">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="ae6bd-155">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)


