---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: 14138dddcd4f4b2150377726d862d953c7360a31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927523"
---
# <span data-ttu-id="ab310-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="ab310-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="ab310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab310-102">SYNOPSIS</span></span>
<span data-ttu-id="ab310-103">Fügen Sie dem Knotentyp die Erweiterung vm hinzu.</span><span class="sxs-lookup"><span data-stu-id="ab310-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="ab310-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab310-104">SYNTAX</span></span>

### <span data-ttu-id="ab310-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="ab310-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab310-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ab310-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab310-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab310-107">DESCRIPTION</span></span>
<span data-ttu-id="ab310-108">Fügen Sie dem Knotentyp die Erweiterung vm hinzu.</span><span class="sxs-lookup"><span data-stu-id="ab310-108">Add vm extension to the node type.</span></span> <span data-ttu-id="ab310-109">Dadurch wird die Erweiterung zur unterliätigen Ressource für den Skalierungssatz für virtuelle Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ab310-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="ab310-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab310-110">EXAMPLES</span></span>

### <span data-ttu-id="ab310-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ab310-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="ab310-112">Mit diesem Befehl wird dem Knotentyp eine Erweiterung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ab310-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="ab310-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ab310-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="ab310-114">Mit diesem Befehl wird dem Knotentyp eine Erweiterung mit Einstellungen und geschützten Einstellungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ab310-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="ab310-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ab310-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="ab310-116">Mit diesem Befehl wird dem Knotentyp eine Erweiterung mit Piping hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ab310-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="ab310-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ab310-117">PARAMETERS</span></span>

### <span data-ttu-id="ab310-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab310-118">-AsJob</span></span>
<span data-ttu-id="ab310-119">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="ab310-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ab310-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ab310-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ab310-121">Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn sie zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ab310-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="ab310-122">Nach der Bereitstellung wird die Erweiterung jedoch nur dann ein Upgrade auf Nebenversionen durchführen, wenn sie erneut bereitgestellt wird, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ab310-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="ab310-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ab310-123">-ClusterName</span></span>
<span data-ttu-id="ab310-124">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="ab310-124">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab310-125">-DefaultProfile</span></span>
<span data-ttu-id="ab310-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab310-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="ab310-127">-ForceUpdateTag</span></span>
<span data-ttu-id="ab310-128">Wenn ein Wert angegeben wird und sich vom vorherigen Wert abwechselt, wird der Erweiterungshandler gezwungen, zu aktualisieren, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="ab310-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab310-129">-InputObject</span></span>
<span data-ttu-id="ab310-130">Knotentypressource</span><span class="sxs-lookup"><span data-stu-id="ab310-130">Node Type resource</span></span>

```yaml
Type: PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-131">-Name</span><span class="sxs-lookup"><span data-stu-id="ab310-131">-Name</span></span>
<span data-ttu-id="ab310-132">Erweiterungsname.</span><span class="sxs-lookup"><span data-stu-id="ab310-132">extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="ab310-133">-NodeTypeName</span></span>
<span data-ttu-id="ab310-134">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="ab310-134">Specify the name of the node type.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="ab310-135">-ProtectedSetting</span></span>
<span data-ttu-id="ab310-136">Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder gar keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="ab310-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="ab310-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="ab310-138">Sammlung von Erweiterungsnamen, nach der diese Erweiterung bereitgestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ab310-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ab310-139">-Publisher</span></span>
<span data-ttu-id="ab310-140">Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="ab310-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="ab310-141">Dies kann das Get-AzVMImagePublisher-Cmdlet verwenden, um den Herausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab310-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab310-142">-ResourceGroupName</span></span>
<span data-ttu-id="ab310-143">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ab310-143">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-144">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="ab310-144">-Setting</span></span>
<span data-ttu-id="ab310-145">Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="ab310-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-146">-Type</span><span class="sxs-lookup"><span data-stu-id="ab310-146">-Type</span></span>
<span data-ttu-id="ab310-147">Gibt den Typ der Erweiterung an. Ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="ab310-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="ab310-148">Sie können das Get-AzVMExtensionImageType-Cmdlet verwenden, um den Erweiterungstyp zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab310-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ab310-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="ab310-150">Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="ab310-150">Specifies the version of the script handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab310-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab310-151">-Confirm</span></span>
<span data-ttu-id="ab310-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab310-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab310-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab310-153">-WhatIf</span></span>
<span data-ttu-id="ab310-154">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab310-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab310-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab310-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab310-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab310-156">CommonParameters</span></span>
<span data-ttu-id="ab310-157">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab310-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab310-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab310-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab310-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab310-159">INPUTS</span></span>

### <span data-ttu-id="ab310-160">System.String</span><span class="sxs-lookup"><span data-stu-id="ab310-160">System.String</span></span>

### <span data-ttu-id="ab310-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ab310-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="ab310-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab310-162">OUTPUTS</span></span>

### <span data-ttu-id="ab310-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ab310-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="ab310-164">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ab310-164">NOTES</span></span>

## <span data-ttu-id="ab310-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ab310-165">RELATED LINKS</span></span>
