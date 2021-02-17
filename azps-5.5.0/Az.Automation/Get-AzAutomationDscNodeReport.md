---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: cc7beb921e09a2cdf1568e9cb693dd01f059e562
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171737"
---
# <span data-ttu-id="27241-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="27241-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="27241-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27241-102">SYNOPSIS</span></span>
<span data-ttu-id="27241-103">Ruft Berichte ab, die von einem DSC-Knoten an die Automatisierung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="27241-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="27241-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27241-104">SYNTAX</span></span>

### <span data-ttu-id="27241-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="27241-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27241-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="27241-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27241-107">ById</span><span class="sxs-lookup"><span data-stu-id="27241-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27241-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27241-108">DESCRIPTION</span></span>
<span data-ttu-id="27241-109">Das **Cmdlet "Get-AzAutomationDscNodeReport"** ruft Berichte ab, die von einem Knoten der APS Desired State Configuration (DSC) an die Azure Automation gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="27241-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="27241-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27241-110">EXAMPLES</span></span>

### <span data-ttu-id="27241-111">Beispiel 1: Alle Berichte für einen DSC-Knoten erhalten</span><span class="sxs-lookup"><span data-stu-id="27241-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="27241-112">Der erste Befehl ruft den DSC-Knoten für den Computer namens "Computer14" im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="27241-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="27241-113">Der Befehl speichert dieses Objekt in der $Node Variable.</span><span class="sxs-lookup"><span data-stu-id="27241-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="27241-114">Der zweite Befehl ruft Metadaten für alle Berichte ab, die vom DSC-Knoten "Computer14" an das Automatisierungskonto namens "Contoso17" gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="27241-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="27241-115">Der Befehl gibt den Knoten mithilfe der **Id-Eigenschaft** des $Node an.</span><span class="sxs-lookup"><span data-stu-id="27241-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="27241-116">Beispiel 2: Erhalten eines Berichts für einen DSC-Knoten nach Berichts-ID</span><span class="sxs-lookup"><span data-stu-id="27241-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="27241-117">Der erste Befehl ruft den DSC-Knoten für den Computer namens "Computer14" im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="27241-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="27241-118">Der Befehl speichert dieses Objekt in der $Node Variable.</span><span class="sxs-lookup"><span data-stu-id="27241-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="27241-119">Der zweite Befehl ruft Metadaten für den Bericht ab, der durch die angegebene ID identifiziert wird, die vom Knoten "DSC" namens "Computer14" an das Automatisierungskonto namens "Contoso17" gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="27241-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="27241-120">Beispiel 3: Erhalten des neuesten Berichts für einen DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="27241-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="27241-121">Der erste Befehl ruft den DSC-Knoten für den Computer namens "Computer14" im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="27241-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="27241-122">Der Befehl speichert dieses Objekt in der $Node Variable.</span><span class="sxs-lookup"><span data-stu-id="27241-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="27241-123">Der zweite Befehl ruft Metadaten für den neuesten Bericht ab, der vom Knoten "DSC" namens "Computer14" an das Automatisierungskonto namens "Contoso17" gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="27241-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="27241-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27241-124">PARAMETERS</span></span>

### <span data-ttu-id="27241-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="27241-125">-AutomationAccountName</span></span>
<span data-ttu-id="27241-126">Gibt den Namen eines Automatisierungskontos an.</span><span class="sxs-lookup"><span data-stu-id="27241-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="27241-127">Dieses Cmdlet exportiert Berichte für einen DSC-Knoten, der zu dem Konto gehört, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="27241-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="27241-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27241-128">-DefaultProfile</span></span>
<span data-ttu-id="27241-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="27241-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27241-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="27241-130">-EndTime</span></span>
<span data-ttu-id="27241-131">Gibt eine Endzeit an.</span><span class="sxs-lookup"><span data-stu-id="27241-131">Specifies an end time.</span></span>
<span data-ttu-id="27241-132">Dieses Cmdlet ruft Berichte ab, die die Automatisierung vor diesem Zeitpunkt erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="27241-132">This cmdlet gets reports that Automation received before this time.</span></span>

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

### <span data-ttu-id="27241-133">-ID</span><span class="sxs-lookup"><span data-stu-id="27241-133">-Id</span></span>
<span data-ttu-id="27241-134">Gibt die eindeutige ID des DSC-Knotenberichts an, den dieses Cmdlet erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="27241-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

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

### <span data-ttu-id="27241-135">-Latest</span><span class="sxs-lookup"><span data-stu-id="27241-135">-Latest</span></span>
<span data-ttu-id="27241-136">Gibt an, dass dieses Cmdlet nur den neuesten DSC-Bericht für den angegebenen Knoten erhält.</span><span class="sxs-lookup"><span data-stu-id="27241-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

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

### <span data-ttu-id="27241-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="27241-137">-NodeId</span></span>
<span data-ttu-id="27241-138">Gibt die eindeutige ID des DSC-Knotens an, für den dieses Cmdlet Berichte erhält.</span><span class="sxs-lookup"><span data-stu-id="27241-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="27241-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27241-139">-ResourceGroupName</span></span>
<span data-ttu-id="27241-140">Gibt den Namen einer Ressourcengruppe an, die den DSC-Knoten enthält, für den dieses Cmdlet Berichte erhält.</span><span class="sxs-lookup"><span data-stu-id="27241-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="27241-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="27241-141">-StartTime</span></span>
<span data-ttu-id="27241-142">Gibt eine Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="27241-142">Specifies a start time.</span></span>
<span data-ttu-id="27241-143">Dieses Cmdlet ruft Berichte ab, die Automatisierung nach diesem Zeitpunkt erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="27241-143">This cmdlet gets reports that Automation received after this time.</span></span>

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

### <span data-ttu-id="27241-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27241-144">CommonParameters</span></span>
<span data-ttu-id="27241-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27241-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27241-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27241-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27241-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27241-147">INPUTS</span></span>

### <span data-ttu-id="27241-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="27241-148">System.Guid</span></span>

### <span data-ttu-id="27241-149">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="27241-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="27241-150">System.String</span><span class="sxs-lookup"><span data-stu-id="27241-150">System.String</span></span>

## <span data-ttu-id="27241-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27241-151">OUTPUTS</span></span>

### <span data-ttu-id="27241-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="27241-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="27241-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="27241-153">NOTES</span></span>

## <span data-ttu-id="27241-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="27241-154">RELATED LINKS</span></span>

[<span data-ttu-id="27241-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="27241-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="27241-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="27241-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


