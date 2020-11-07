---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: 05a4ce9fdaeebc447be0d8f1e6162399f964043f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650424"
---
# <span data-ttu-id="403dc-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="403dc-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="403dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="403dc-102">SYNOPSIS</span></span>
<span data-ttu-id="403dc-103">Ändert eine Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="403dc-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="403dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="403dc-104">SYNTAX</span></span>

### <span data-ttu-id="403dc-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="403dc-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="403dc-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="403dc-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="403dc-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="403dc-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="403dc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="403dc-108">DESCRIPTION</span></span>
<span data-ttu-id="403dc-109">Das Set-AzAnalysisServicesServer-Cmdlet ändert eine Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="403dc-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="403dc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="403dc-110">EXAMPLES</span></span>

### <span data-ttu-id="403dc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="403dc-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="403dc-112">Ändert den Server mit dem Namen "Testserver" in der ResourceGroup-Testgruppe, um die Tags als key1: value1 und key2: Value2 und Administrator auf testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="403dc-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="403dc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="403dc-113">PARAMETERS</span></span>

### <span data-ttu-id="403dc-114">– Administrator</span><span class="sxs-lookup"><span data-stu-id="403dc-114">-Administrator</span></span>
<span data-ttu-id="403dc-115">Eine Zeichenfolge, die eine durch Kommas getrennte Liste der Benutzer oder Gruppen darstellt, die als Administratoren auf dem Server eingerichtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="403dc-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="403dc-116">Die Benutzer oder Gruppen müssen als UPN-Format angegeben werden, beispielsweise user@contoso.com oder groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="403dc-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="403dc-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="403dc-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="403dc-118">Der BLOB-Container-URI für die Sicherung des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="403dc-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="403dc-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="403dc-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="403dc-120">Standardverbindungsmodus eines Analysis Service-Servers</span><span class="sxs-lookup"><span data-stu-id="403dc-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="403dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="403dc-121">-DefaultProfile</span></span>
<span data-ttu-id="403dc-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="403dc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="403dc-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="403dc-123">-DisableBackup</span></span>
<span data-ttu-id="403dc-124">Der Schalter zum Deaktivieren des BLOB-Sicherungs Containers.</span><span class="sxs-lookup"><span data-stu-id="403dc-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="403dc-125">Um den BLOB-Sicherungs Container wieder zu aktivieren, geben Sie den BLOB-Sicherungs Container-URI als-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="403dc-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="403dc-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="403dc-126">-DisassociateGateway</span></span>
<span data-ttu-id="403dc-127">Aufheben der Zuordnung von Gateway-Ressourcen zu einem Analysis-Server</span><span class="sxs-lookup"><span data-stu-id="403dc-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="403dc-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="403dc-128">-FirewallConfig</span></span>
<span data-ttu-id="403dc-129">Firewall-Konfiguration eines Analysis-Servers</span><span class="sxs-lookup"><span data-stu-id="403dc-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="403dc-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="403dc-130">-GatewayResourceId</span></span>
<span data-ttu-id="403dc-131">Gateway-Ressourcen-ID für assocaite zu einem Analysis-Server</span><span class="sxs-lookup"><span data-stu-id="403dc-131">Gateway resource Id for assocaite to an Analysis server</span></span>

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

### <span data-ttu-id="403dc-132">-Name</span><span class="sxs-lookup"><span data-stu-id="403dc-132">-Name</span></span>
<span data-ttu-id="403dc-133">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="403dc-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="403dc-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="403dc-134">-PassThru</span></span>
<span data-ttu-id="403dc-135">Gibt die gelöschten Serverdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="403dc-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="403dc-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="403dc-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="403dc-137">Anzahl der Replikate eines Analysis-Service-Servers nur lesen</span><span class="sxs-lookup"><span data-stu-id="403dc-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="403dc-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="403dc-138">-ResourceGroupName</span></span>
<span data-ttu-id="403dc-139">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="403dc-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="403dc-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="403dc-140">-Sku</span></span>
<span data-ttu-id="403dc-141">Der Name der SKU für den Server.</span><span class="sxs-lookup"><span data-stu-id="403dc-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="403dc-142">Die unterstützten Werte sind 0 ', ist 1 ', ist 2 ', ist 4 ' für die Standard Ebene; "B1", "B2" für die grundlegende Ebene und 'd 1 für die Entwicklungsstufe.</span><span class="sxs-lookup"><span data-stu-id="403dc-142">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="403dc-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="403dc-143">-Tag</span></span>
<span data-ttu-id="403dc-144">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="403dc-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="403dc-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="403dc-145">-Confirm</span></span>
<span data-ttu-id="403dc-146">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="403dc-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="403dc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="403dc-147">-WhatIf</span></span>
<span data-ttu-id="403dc-148">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="403dc-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="403dc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="403dc-149">CommonParameters</span></span>
<span data-ttu-id="403dc-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="403dc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="403dc-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="403dc-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="403dc-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="403dc-152">INPUTS</span></span>

### <span data-ttu-id="403dc-153">System. String</span><span class="sxs-lookup"><span data-stu-id="403dc-153">System.String</span></span>

### <span data-ttu-id="403dc-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="403dc-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="403dc-155">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="403dc-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="403dc-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="403dc-156">System.Int32</span></span>

### <span data-ttu-id="403dc-157">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="403dc-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="403dc-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="403dc-158">OUTPUTS</span></span>

### <span data-ttu-id="403dc-159">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="403dc-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="403dc-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="403dc-160">NOTES</span></span>
<span data-ttu-id="403dc-161">Alias: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="403dc-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="403dc-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="403dc-162">RELATED LINKS</span></span>

[<span data-ttu-id="403dc-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="403dc-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="403dc-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="403dc-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
