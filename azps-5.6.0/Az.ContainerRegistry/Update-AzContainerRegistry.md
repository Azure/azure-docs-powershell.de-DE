---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: aa84186be2b5dc13117397e76722a6826d5314a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920771"
---
# <span data-ttu-id="9f3fe-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9f3fe-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="9f3fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="9f3fe-103">Aktualisiert eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-103">Updates a container registry.</span></span>

## <span data-ttu-id="9f3fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f3fe-104">SYNTAX</span></span>

### <span data-ttu-id="9f3fe-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f3fe-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f3fe-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f3fe-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f3fe-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f3fe-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f3fe-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f3fe-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f3fe-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f3fe-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f3fe-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f3fe-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f3fe-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f3fe-111">DESCRIPTION</span></span>
<span data-ttu-id="9f3fe-112">Das Update-AzContainerRegistry cmdlet aktualisiert eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="9f3fe-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f3fe-113">EXAMPLES</span></span>

### <span data-ttu-id="9f3fe-114">Beispiel 1: Aktivieren des Administratorbenutzers für eine angegebene Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="9f3fe-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="9f3fe-115">Dieser Befehl aktiviert den Administratorbenutzer für die angegebene Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="9f3fe-116">Beispiel 2: Festlegen des speicherkontos, das von einer angegebenen Containerregistrierung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="9f3fe-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="9f3fe-117">Mit diesem Befehl wird die angegebene Containerregistrierung so festgelegt, dass ein vorhandenes Speicherkonto \` mystorageaccount \` im gleichen Abonnement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="9f3fe-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f3fe-118">PARAMETERS</span></span>

### <span data-ttu-id="9f3fe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f3fe-119">-DefaultProfile</span></span>
<span data-ttu-id="9f3fe-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9f3fe-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f3fe-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="9f3fe-121">-DisableAdminUser</span></span>
<span data-ttu-id="9f3fe-122">Aktivieren Sie Administratorbenutzer für die Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3fe-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="9f3fe-123">-EnableAdminUser</span></span>
<span data-ttu-id="9f3fe-124">Aktivieren Sie Administratorbenutzer für die Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3fe-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9f3fe-125">-Name</span></span>
<span data-ttu-id="9f3fe-126">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f3fe-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9f3fe-127">-NetworkRuleSet</span></span>
<span data-ttu-id="9f3fe-128">Die Netzwerkregel für eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-128">The network rule set for a container registry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f3fe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f3fe-129">-ResourceGroupName</span></span>
<span data-ttu-id="9f3fe-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f3fe-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f3fe-131">-ResourceId</span></span>
<span data-ttu-id="9f3fe-132">Die Containerregistrierungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="9f3fe-132">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f3fe-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="9f3fe-133">-Sku</span></span>
<span data-ttu-id="9f3fe-134">Containerregistrierungs-SKU.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-134">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3fe-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9f3fe-135">-StorageAccountName</span></span>
<span data-ttu-id="9f3fe-136">Der Name eines vorhandenen Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-136">The name of an existing storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3fe-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f3fe-137">-Tag</span></span>
<span data-ttu-id="9f3fe-138">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="9f3fe-139">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="9f3fe-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3fe-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f3fe-140">-Confirm</span></span>
<span data-ttu-id="9f3fe-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3fe-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f3fe-142">-WhatIf</span></span>
<span data-ttu-id="9f3fe-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f3fe-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3fe-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f3fe-145">CommonParameters</span></span>
<span data-ttu-id="9f3fe-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f3fe-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f3fe-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f3fe-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f3fe-148">INPUTS</span></span>

### <span data-ttu-id="9f3fe-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9f3fe-149">System.String</span></span>

## <span data-ttu-id="9f3fe-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f3fe-150">OUTPUTS</span></span>

### <span data-ttu-id="9f3fe-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9f3fe-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="9f3fe-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9f3fe-152">NOTES</span></span>

## <span data-ttu-id="9f3fe-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9f3fe-153">RELATED LINKS</span></span>

[<span data-ttu-id="9f3fe-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9f3fe-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="9f3fe-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9f3fe-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="9f3fe-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9f3fe-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

