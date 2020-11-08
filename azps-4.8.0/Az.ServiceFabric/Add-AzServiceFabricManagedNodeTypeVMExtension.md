---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174166"
---
# <span data-ttu-id="695c7-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="695c7-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="695c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="695c7-102">SYNOPSIS</span></span>
<span data-ttu-id="695c7-103">Fügen Sie dem Knotentyp eine VM-Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="695c7-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="695c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="695c7-104">SYNTAX</span></span>

### <span data-ttu-id="695c7-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="695c7-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="695c7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="695c7-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="695c7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="695c7-107">DESCRIPTION</span></span>
<span data-ttu-id="695c7-108">Fügen Sie dem Knotentyp eine VM-Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="695c7-108">Add vm extension to the node type.</span></span> <span data-ttu-id="695c7-109">Dadurch wird die Erweiterung der Skalierungs Satz Ressource underliying Virtual Machine hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="695c7-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="695c7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="695c7-110">EXAMPLES</span></span>

### <span data-ttu-id="695c7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="695c7-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="695c7-112">Mit diesem Befehl wird dem Knotentyp eine Erweiterung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="695c7-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="695c7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="695c7-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="695c7-114">Mit diesem Befehl wird dem Knotentyp eine Erweiterung mit Einstellungen und geschützten Einstellungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="695c7-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="695c7-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="695c7-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="695c7-116">Mit diesem Befehl wird dem Knotentyp eine Erweiterung mit Piping hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="695c7-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="695c7-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="695c7-117">PARAMETERS</span></span>

### <span data-ttu-id="695c7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="695c7-118">-AsJob</span></span>
<span data-ttu-id="695c7-119">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="695c7-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="695c7-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="695c7-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="695c7-121">Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="695c7-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="695c7-122">Nach der Bereitstellung werden die Erweiterungen jedoch nur dann untergeordnete Versionen aktualisiert, wenn Sie erneut bereitgestellt werden, auch wenn diese Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="695c7-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="695c7-123">-Clustername</span><span class="sxs-lookup"><span data-stu-id="695c7-123">-ClusterName</span></span>
<span data-ttu-id="695c7-124">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="695c7-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="695c7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695c7-125">-DefaultProfile</span></span>
<span data-ttu-id="695c7-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="695c7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="695c7-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="695c7-127">-ForceUpdateTag</span></span>
<span data-ttu-id="695c7-128">Wenn ein Wert angegeben wird, der vom vorherigen Wert abweicht, wird der Erweiterungshandler auch dann aktualisiert, wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="695c7-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="695c7-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="695c7-129">-InputObject</span></span>
<span data-ttu-id="695c7-130">Knotentyp Ressource</span><span class="sxs-lookup"><span data-stu-id="695c7-130">Node Type resource</span></span>

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

### <span data-ttu-id="695c7-131">-Name</span><span class="sxs-lookup"><span data-stu-id="695c7-131">-Name</span></span>
<span data-ttu-id="695c7-132">Name der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="695c7-132">extension name.</span></span>

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

### <span data-ttu-id="695c7-133">-NodeType</span><span class="sxs-lookup"><span data-stu-id="695c7-133">-NodeTypeName</span></span>
<span data-ttu-id="695c7-134">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="695c7-134">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="695c7-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="695c7-135">-ProtectedSetting</span></span>
<span data-ttu-id="695c7-136">Die Erweiterung kann entweder protectedSettings oder protectedSettingsFromKeyVault oder keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="695c7-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="695c7-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="695c7-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="695c7-138">Sammlung von Erweiterungsnamen, nach denen diese Erweiterung bereitgestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="695c7-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="695c7-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="695c7-139">-Publisher</span></span>
<span data-ttu-id="695c7-140">Der Name des Erweiterungs Handlers Publisher.</span><span class="sxs-lookup"><span data-stu-id="695c7-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="695c7-141">Dies kann das Get-AzVMImagePublisher-Cmdlet verwenden, um den Verleger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="695c7-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="695c7-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="695c7-142">-ResourceGroupName</span></span>
<span data-ttu-id="695c7-143">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="695c7-143">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="695c7-144">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="695c7-144">-Setting</span></span>
<span data-ttu-id="695c7-145">Mit JSON formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="695c7-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="695c7-146">-Typ</span><span class="sxs-lookup"><span data-stu-id="695c7-146">-Type</span></span>
<span data-ttu-id="695c7-147">Gibt den Typ der Erweiterung an; ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="695c7-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="695c7-148">Sie können das Get-AzVMExtensionImageType-Cmdlet verwenden, um den Erweiterungstyp abzurufen.</span><span class="sxs-lookup"><span data-stu-id="695c7-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="695c7-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="695c7-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="695c7-150">Gibt die Version des Skript Handlers an.</span><span class="sxs-lookup"><span data-stu-id="695c7-150">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="695c7-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="695c7-151">-Confirm</span></span>
<span data-ttu-id="695c7-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="695c7-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="695c7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="695c7-153">-WhatIf</span></span>
<span data-ttu-id="695c7-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="695c7-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="695c7-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="695c7-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="695c7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695c7-156">CommonParameters</span></span>
<span data-ttu-id="695c7-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="695c7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695c7-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="695c7-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695c7-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="695c7-159">INPUTS</span></span>

### <span data-ttu-id="695c7-160">System. String</span><span class="sxs-lookup"><span data-stu-id="695c7-160">System.String</span></span>

### <span data-ttu-id="695c7-161">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="695c7-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="695c7-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="695c7-162">OUTPUTS</span></span>

### <span data-ttu-id="695c7-163">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="695c7-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="695c7-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="695c7-164">NOTES</span></span>

## <span data-ttu-id="695c7-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="695c7-165">RELATED LINKS</span></span>
