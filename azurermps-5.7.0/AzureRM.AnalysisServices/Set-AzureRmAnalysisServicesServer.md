---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/set-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 485687b0a08ca69edc77b4ee5f9510ad8a1396a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479814"
---
# <span data-ttu-id="265b8-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="265b8-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="265b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="265b8-102">SYNOPSIS</span></span>
<span data-ttu-id="265b8-103">Ändert eine Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="265b8-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="265b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="265b8-104">SYNTAX</span></span>

### <span data-ttu-id="265b8-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="265b8-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="265b8-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="265b8-106">DisableBackup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="265b8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="265b8-107">DESCRIPTION</span></span>
<span data-ttu-id="265b8-108">Das Set-AzureRmAnalysisServicesServer-Cmdlet ändert eine Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="265b8-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="265b8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="265b8-109">EXAMPLES</span></span>

### <span data-ttu-id="265b8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="265b8-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="265b8-111">Ändert den Server mit dem Namen "Testserver" in der ResourceGroup-Testgruppe, um die Tags als key1: value1 und key2: Value2 und Administrator auf testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="265b8-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="265b8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="265b8-112">PARAMETERS</span></span>

### <span data-ttu-id="265b8-113">– Administrator</span><span class="sxs-lookup"><span data-stu-id="265b8-113">-Administrator</span></span>
<span data-ttu-id="265b8-114">Eine Zeichenfolge, die eine durch Kommas getrennte Liste der Benutzer oder Gruppen darstellt, die als Administratoren auf dem Server eingerichtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="265b8-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="265b8-115">Die Benutzer oder Gruppen müssen als UPN-Format angegeben werden, beispielsweise user@contoso.com oder groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="265b8-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265b8-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="265b8-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="265b8-117">Der BLOB-Container-URI für die Sicherung des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="265b8-117">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="265b8-118">-DefaultProfile</span></span>
<span data-ttu-id="265b8-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="265b8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="265b8-120">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="265b8-120">-DisableBackup</span></span>
<span data-ttu-id="265b8-121">Der Schalter zum Deaktivieren des BLOB-Sicherungs Containers.</span><span class="sxs-lookup"><span data-stu-id="265b8-121">The switch to disable backup blob container.</span></span>
<span data-ttu-id="265b8-122">Um den BLOB-Sicherungs Container wieder zu aktivieren, geben Sie den BLOB-Sicherungs Container-URI als-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="265b8-122">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBackup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265b8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="265b8-123">-Name</span></span>
<span data-ttu-id="265b8-124">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="265b8-124">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="265b8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="265b8-125">-PassThru</span></span>
<span data-ttu-id="265b8-126">Gibt die gelöschten Serverdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="265b8-126">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="265b8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="265b8-127">-ResourceGroupName</span></span>
<span data-ttu-id="265b8-128">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="265b8-128">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265b8-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="265b8-129">-Sku</span></span>
<span data-ttu-id="265b8-130">Der Name der SKU für den Server.</span><span class="sxs-lookup"><span data-stu-id="265b8-130">The name of the Sku for the server.</span></span>
<span data-ttu-id="265b8-131">Die unterstützten Werte sind 0 ', ist 1 ', ist 2 ', ist 4 ' für die Standard Ebene; "B1", "B2" für die grundlegende Ebene und 'd 1 für die Entwicklungsstufe.</span><span class="sxs-lookup"><span data-stu-id="265b8-131">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265b8-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="265b8-132">-Tag</span></span>
<span data-ttu-id="265b8-133">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="265b8-133">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265b8-134">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="265b8-134">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="265b8-135">Anzahl der Replikate eines Analysis-Service-Servers nur lesen</span><span class="sxs-lookup"><span data-stu-id="265b8-135">Read only replica count of an Analysis service server</span></span>

```yaml
Type: Integer
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265b8-136">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="265b8-136">-DefaultConnectionMode</span></span>
<span data-ttu-id="265b8-137">Standardverbindungsmodus eines Analysis Service-Servers</span><span class="sxs-lookup"><span data-stu-id="265b8-137">Default connection mode of an Analysis service server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265b8-138">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="265b8-138">-FirewallConfig</span></span>
<span data-ttu-id="265b8-139">Firewall-Konfiguration eines Analysis-Servers</span><span class="sxs-lookup"><span data-stu-id="265b8-139">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265b8-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="265b8-140">-Confirm</span></span>
<span data-ttu-id="265b8-141">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="265b8-141">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="265b8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="265b8-142">-WhatIf</span></span>
<span data-ttu-id="265b8-143">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="265b8-143">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="265b8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="265b8-144">CommonParameters</span></span>
<span data-ttu-id="265b8-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="265b8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="265b8-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="265b8-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="265b8-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="265b8-147">INPUTS</span></span>

### <span data-ttu-id="265b8-148">Keine</span><span class="sxs-lookup"><span data-stu-id="265b8-148">None</span></span>
<span data-ttu-id="265b8-149">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="265b8-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="265b8-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="265b8-150">OUTPUTS</span></span>

### <span data-ttu-id="265b8-151">Microsoft. Azure. Management. Analysis. Models. AnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="265b8-151">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="265b8-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="265b8-152">NOTES</span></span>
<span data-ttu-id="265b8-153">Alias: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="265b8-153">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="265b8-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="265b8-154">RELATED LINKS</span></span>

[<span data-ttu-id="265b8-155">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="265b8-155">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="265b8-156">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="265b8-156">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
