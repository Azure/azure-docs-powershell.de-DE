---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: b39da37f41e3a18bc70f25fe36d67301e49867c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922267"
---
# <span data-ttu-id="88754-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="88754-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="88754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88754-102">SYNOPSIS</span></span>
<span data-ttu-id="88754-103">Ändert eine Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="88754-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="88754-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88754-104">SYNTAX</span></span>

### <span data-ttu-id="88754-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="88754-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88754-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="88754-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88754-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="88754-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88754-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88754-108">DESCRIPTION</span></span>
<span data-ttu-id="88754-109">Das Set-AzAnalysisServicesServer-Cmdlet ändert eine Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="88754-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="88754-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88754-110">EXAMPLES</span></span>

### <span data-ttu-id="88754-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="88754-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="88754-112">Ändert den Server namens Testserver in der Ressourcengruppentestgruppe, um die Tags als key1:value1 und key2:value2 und administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="88754-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="88754-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="88754-113">PARAMETERS</span></span>

### <span data-ttu-id="88754-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="88754-114">-Administrator</span></span>
<span data-ttu-id="88754-115">Eine Zeichenfolge, die eine durch Kommas getrennte Liste der Benutzer oder Gruppen darstellt, die als Administratoren auf dem Server festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="88754-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="88754-116">Die Benutzer oder Gruppen müssen ein UPN-Format angegeben werden, z. B. user@contoso.com oder groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="88754-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88754-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="88754-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="88754-118">Der Blobcontainer-Uri für die Sicherung des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="88754-118">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88754-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="88754-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="88754-120">Standardverbindungsmodus eines Analysedienstservers</span><span class="sxs-lookup"><span data-stu-id="88754-120">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88754-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88754-121">-DefaultProfile</span></span>
<span data-ttu-id="88754-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88754-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88754-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="88754-123">-DisableBackup</span></span>
<span data-ttu-id="88754-124">Der Schalter zum Deaktivieren des Sicherungsblobcontainers.</span><span class="sxs-lookup"><span data-stu-id="88754-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="88754-125">Um den Sicherungsblobcontainer erneut zu aktivieren, stellen Sie den Uri für den Sicherungsblobcontainer als -BackupBlobContainerUri zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="88754-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBackup
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88754-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="88754-126">-DisassociateGateway</span></span>
<span data-ttu-id="88754-127">Assoziieren der Gatewayressource von einem Analyseserver</span><span class="sxs-lookup"><span data-stu-id="88754-127">Disassociate Gateway resource from an Analysis server</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisassociateGateway
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88754-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="88754-128">-FirewallConfig</span></span>
<span data-ttu-id="88754-129">Firewallkonfiguration eines Analyseservers</span><span class="sxs-lookup"><span data-stu-id="88754-129">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88754-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="88754-130">-GatewayResourceId</span></span>
<span data-ttu-id="88754-131">Gatewayressourcen-ID, die einem Analyseserver zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="88754-131">Gateway resource Id to associate to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88754-132">-Name</span><span class="sxs-lookup"><span data-stu-id="88754-132">-Name</span></span>
<span data-ttu-id="88754-133">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="88754-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="88754-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88754-134">-PassThru</span></span>
<span data-ttu-id="88754-135">Gibt die gelöschten Serverdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="88754-135">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88754-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="88754-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="88754-137">Schreibgeschützte Replikatanzahl eines Analysis Service Servers</span><span class="sxs-lookup"><span data-stu-id="88754-137">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88754-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88754-138">-ResourceGroupName</span></span>
<span data-ttu-id="88754-139">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="88754-139">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88754-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="88754-140">-Sku</span></span>
<span data-ttu-id="88754-141">Der Name der Sku für den Server.</span><span class="sxs-lookup"><span data-stu-id="88754-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="88754-142">Die unterstützten Werte sind "S0", "S1", "S2", "S4", "S8", "S9", "S8v2", "S9v2" für die Standardebene; "B1", "B2" für die Ebene "Basic" und "D1" für die Entwicklungsebene.</span><span class="sxs-lookup"><span data-stu-id="88754-142">The supported values are 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88754-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="88754-143">-Tag</span></span>
<span data-ttu-id="88754-144">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="88754-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88754-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88754-145">-Confirm</span></span>
<span data-ttu-id="88754-146">Fordert den Benutzer auf, zu bestätigen, ob er den Vorgang ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="88754-146">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88754-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88754-147">-WhatIf</span></span>
<span data-ttu-id="88754-148">Beschreibt die Aktionen, die der aktuelle Vorgang ausführen soll, ohne sie tatsächlich durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="88754-148">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88754-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88754-149">CommonParameters</span></span>
<span data-ttu-id="88754-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88754-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88754-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88754-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88754-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88754-152">INPUTS</span></span>

### <span data-ttu-id="88754-153">System.String</span><span class="sxs-lookup"><span data-stu-id="88754-153">System.String</span></span>

### <span data-ttu-id="88754-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="88754-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="88754-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="88754-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="88754-156">System.Int32</span><span class="sxs-lookup"><span data-stu-id="88754-156">System.Int32</span></span>

### <span data-ttu-id="88754-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="88754-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="88754-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88754-158">OUTPUTS</span></span>

### <span data-ttu-id="88754-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="88754-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="88754-160">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="88754-160">NOTES</span></span>
<span data-ttu-id="88754-161">Alias: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="88754-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="88754-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="88754-162">RELATED LINKS</span></span>

[<span data-ttu-id="88754-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="88754-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="88754-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="88754-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
