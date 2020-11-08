---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: 81a50a8c805d05b47b934b899eff708031ac6beb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165342"
---
# <span data-ttu-id="09c09-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="09c09-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="09c09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09c09-102">SYNOPSIS</span></span>
<span data-ttu-id="09c09-103">Ruft Berichte ab, die von einem DSC-Knoten an die Automatisierung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="09c09-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="09c09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09c09-104">SYNTAX</span></span>

### <span data-ttu-id="09c09-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="09c09-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09c09-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="09c09-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09c09-107">ById</span><span class="sxs-lookup"><span data-stu-id="09c09-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09c09-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09c09-108">DESCRIPTION</span></span>
<span data-ttu-id="09c09-109">Das Cmdlet " **Get-AzAutomationDscNodeReport** " ruft Berichte ab, die von einem APS-Knoten (Desired State Configuration, DSC) an Azure Automation gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="09c09-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="09c09-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09c09-110">EXAMPLES</span></span>

### <span data-ttu-id="09c09-111">Beispiel 1: Abrufen aller Berichte für einen DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="09c09-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="09c09-112">Der erste Befehl ruft den DSC-Knoten für den Computer mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="09c09-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="09c09-113">Der Befehl speichert dieses Objekt in der $Node-Variablen.</span><span class="sxs-lookup"><span data-stu-id="09c09-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="09c09-114">Der zweite Befehl ruft Metadaten für alle Berichte ab, die vom DSC-Knoten mit dem Namen Computer14 an das Automatisierungs Konto mit dem Namen Contoso17 gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="09c09-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="09c09-115">Der Befehl gibt den Knoten mithilfe der **ID** -Eigenschaft des $Node-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="09c09-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="09c09-116">Beispiel 2: Abrufen eines Berichts für einen DSC-Knoten nach Berichts-ID</span><span class="sxs-lookup"><span data-stu-id="09c09-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="09c09-117">Der erste Befehl ruft den DSC-Knoten für den Computer mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="09c09-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="09c09-118">Der Befehl speichert dieses Objekt in der $Node-Variablen.</span><span class="sxs-lookup"><span data-stu-id="09c09-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="09c09-119">Der zweite Befehl ruft Metadaten für den Bericht ab, der durch die angegebene ID identifiziert wird, die vom DSC-Knoten mit dem Namen Computer14 an das Automatisierungs Konto mit dem Namen Contoso17 gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="09c09-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="09c09-120">Beispiel 3: Abrufen des neuesten Berichts für einen DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="09c09-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="09c09-121">Der erste Befehl ruft den DSC-Knoten für den Computer mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="09c09-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="09c09-122">Der Befehl speichert dieses Objekt in der $Node-Variablen.</span><span class="sxs-lookup"><span data-stu-id="09c09-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="09c09-123">Der zweite Befehl ruft Metadaten für den neuesten Bericht ab, der vom DSC-Knoten mit dem Namen Computer14 an das Automatisierungs Konto mit dem Namen Contoso17 gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="09c09-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="09c09-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="09c09-124">PARAMETERS</span></span>

### <span data-ttu-id="09c09-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="09c09-125">-AutomationAccountName</span></span>
<span data-ttu-id="09c09-126">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="09c09-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="09c09-127">Dieses Cmdlet exportiert Berichte für einen DSC-Knoten, der zu dem Konto gehört, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="09c09-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c09-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c09-128">-DefaultProfile</span></span>
<span data-ttu-id="09c09-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="09c09-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c09-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="09c09-130">-EndTime</span></span>
<span data-ttu-id="09c09-131">Gibt eine Endzeit an.</span><span class="sxs-lookup"><span data-stu-id="09c09-131">Specifies an end time.</span></span>
<span data-ttu-id="09c09-132">Dieses Cmdlet ruft Berichte ab, die von der Automatisierung vor diesem Zeitpunkt empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="09c09-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c09-133">-ID</span><span class="sxs-lookup"><span data-stu-id="09c09-133">-Id</span></span>
<span data-ttu-id="09c09-134">Gibt die eindeutige ID des DSC-Knoten Berichts an, der für dieses Cmdlet abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="09c09-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c09-135">-Neueste</span><span class="sxs-lookup"><span data-stu-id="09c09-135">-Latest</span></span>
<span data-ttu-id="09c09-136">Gibt an, dass dieses Cmdlet nur den neuesten DSC-Bericht für den angegebenen Knoten abruft.</span><span class="sxs-lookup"><span data-stu-id="09c09-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c09-137">-Knoten-Nr</span><span class="sxs-lookup"><span data-stu-id="09c09-137">-NodeId</span></span>
<span data-ttu-id="09c09-138">Gibt die eindeutige ID des DSC-Knotens an, für den dieses Cmdlet Berichte abruft.</span><span class="sxs-lookup"><span data-stu-id="09c09-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c09-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09c09-139">-ResourceGroupName</span></span>
<span data-ttu-id="09c09-140">Gibt den Namen einer Ressourcengruppe an, die den DSC-Knoten enthält, für den dieses Cmdlet Berichte abruft.</span><span class="sxs-lookup"><span data-stu-id="09c09-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c09-141">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="09c09-141">-StartTime</span></span>
<span data-ttu-id="09c09-142">Gibt eine Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="09c09-142">Specifies a start time.</span></span>
<span data-ttu-id="09c09-143">Dieses Cmdlet ruft Berichte ab, die von der Automatisierung nach diesem Zeitpunkt empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="09c09-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c09-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c09-144">CommonParameters</span></span>
<span data-ttu-id="09c09-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09c09-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c09-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09c09-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c09-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09c09-147">INPUTS</span></span>

### <span data-ttu-id="09c09-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="09c09-148">System.Guid</span></span>

### <span data-ttu-id="09c09-149">System. Nullable ' 1 [[System. DateTimeOffset, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="09c09-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="09c09-150">System. String</span><span class="sxs-lookup"><span data-stu-id="09c09-150">System.String</span></span>

## <span data-ttu-id="09c09-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09c09-151">OUTPUTS</span></span>

### <span data-ttu-id="09c09-152">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="09c09-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="09c09-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="09c09-153">NOTES</span></span>

## <span data-ttu-id="09c09-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09c09-154">RELATED LINKS</span></span>

[<span data-ttu-id="09c09-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="09c09-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="09c09-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="09c09-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


