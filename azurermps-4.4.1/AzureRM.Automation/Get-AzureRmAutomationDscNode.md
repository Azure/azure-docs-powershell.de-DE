---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
ms.openlocfilehash: 51d7df7f6b1e99188e5be31537700f4eef019053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498009"
---
# <span data-ttu-id="a9576-101">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a9576-101">Get-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="a9576-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9576-102">SYNOPSIS</span></span>
<span data-ttu-id="a9576-103">Ruft DSC-Knoten aus der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="a9576-103">Gets DSC nodes from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9576-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9576-104">SYNTAX</span></span>

### <span data-ttu-id="a9576-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9576-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9576-106">ById</span><span class="sxs-lookup"><span data-stu-id="a9576-106">ById</span></span>
```
Get-AzureRmAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9576-107">ByName</span><span class="sxs-lookup"><span data-stu-id="a9576-107">ByName</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9576-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9576-108">ByNodeConfiguration</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9576-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9576-109">ByConfiguration</span></span>
```
Get-AzureRmAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9576-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9576-110">DESCRIPTION</span></span>
<span data-ttu-id="a9576-111">Das Cmdlet " **Get-AzureRmAutomationDscNode** " ruft APS-Knoten (Desired State Configuration, DSC) aus Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="a9576-111">The **Get-AzureRmAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="a9576-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9576-112">EXAMPLES</span></span>

### <span data-ttu-id="a9576-113">Beispiel 1: Abrufen aller DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="a9576-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="a9576-114">Dieser Befehl ruft Metadaten für alle DSC-Knoten im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="a9576-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a9576-115">Beispiel 2: Abrufen aller DSC-Knoten für eine DSC-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a9576-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="a9576-116">Dieser Befehl ruft Metadaten für alle DSC-Knoten im Automatisierungs Konto mit dem Namen Contoso17 ab, die einer DSC-Knoten Konfiguration zugeordnet sind, die durch DSC-Konfigurations ContosoConfiguration generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a9576-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="a9576-117">Beispiel 3: Abrufen eines DSC-Knotens anhand der ID</span><span class="sxs-lookup"><span data-stu-id="a9576-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="a9576-118">Dieser Befehl ruft Metadaten auf einem DSC-Knoten mit der angegebenen ID im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="a9576-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a9576-119">Beispiel 4: Abrufen eines DSC-Knotens anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="a9576-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="a9576-120">Dieser Befehl ruft Metadaten auf einem DSC-Knoten mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="a9576-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a9576-121">Beispiel 5: Abrufen aller DSC-Knoten, die einer DSC-Knoten Konfiguration zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="a9576-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="a9576-122">Dieser Befehl ruft Metadaten für alle DSC-Knoten im Automatisierungs Konto mit dem Namen Contoso17 ab, die einer DSC-Knoten Konfiguration mit dem Namen ContosoConfiguration. Webserver zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a9576-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="a9576-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9576-123">PARAMETERS</span></span>

### <span data-ttu-id="a9576-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a9576-124">-AutomationAccountName</span></span>
<span data-ttu-id="a9576-125">Gibt den Namen des Automatisierungs Kontos an, das die DSC-Knoten enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a9576-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a9576-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a9576-126">-ConfigurationName</span></span>
<span data-ttu-id="a9576-127">Gibt den Namen einer DSC-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="a9576-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="a9576-128">Dieses Cmdlet ruft DSC-Knoten ab, die den Knoten Konfigurationen entsprechen, die aus der von diesem Parameter festgelegten Konfiguration generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="a9576-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9576-129">-ID</span><span class="sxs-lookup"><span data-stu-id="a9576-129">-Id</span></span>
<span data-ttu-id="a9576-130">Gibt die eindeutige ID des DSC-Knotens an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a9576-130">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9576-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a9576-131">-Name</span></span>
<span data-ttu-id="a9576-132">Gibt den Namen eines DSC-Knotens an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a9576-132">Specifies the name of a DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9576-133">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a9576-133">-NodeConfigurationName</span></span>
<span data-ttu-id="a9576-134">Gibt den Namen einer Knoten Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a9576-134">Specifies the name of a node configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9576-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9576-135">-ResourceGroupName</span></span>
<span data-ttu-id="a9576-136">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet DSC-Knoten erhält.</span><span class="sxs-lookup"><span data-stu-id="a9576-136">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="a9576-137">-Status</span><span class="sxs-lookup"><span data-stu-id="a9576-137">-Status</span></span>
<span data-ttu-id="a9576-138">Gibt den Status der DSC-Knoten an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a9576-138">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="a9576-139">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a9576-139">Valid values are:</span></span> 

- <span data-ttu-id="a9576-140">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="a9576-140">Compliant</span></span> 
- <span data-ttu-id="a9576-141">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="a9576-141">NotCompliant</span></span>
- <span data-ttu-id="a9576-142">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="a9576-142">Failed</span></span>
- <span data-ttu-id="a9576-143">Ausstehend</span><span class="sxs-lookup"><span data-stu-id="a9576-143">Pending</span></span> 
- <span data-ttu-id="a9576-144">Empfangen</span><span class="sxs-lookup"><span data-stu-id="a9576-144">Received</span></span>
- <span data-ttu-id="a9576-145">Reagiert</span><span class="sxs-lookup"><span data-stu-id="a9576-145">Unresponsive</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases: 
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9576-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9576-146">-DefaultProfile</span></span>
<span data-ttu-id="a9576-147">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9576-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9576-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9576-148">CommonParameters</span></span>
<span data-ttu-id="a9576-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9576-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9576-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9576-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9576-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9576-151">INPUTS</span></span>

## <span data-ttu-id="a9576-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9576-152">OUTPUTS</span></span>

### <span data-ttu-id="a9576-153">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="a9576-153">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="a9576-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9576-154">NOTES</span></span>

## <span data-ttu-id="a9576-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9576-155">RELATED LINKS</span></span>

[<span data-ttu-id="a9576-156">Registrieren-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a9576-156">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="a9576-157">Satz-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a9576-157">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="a9576-158">Registrierung aufheben-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a9576-158">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


