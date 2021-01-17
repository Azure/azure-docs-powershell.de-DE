---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472872"
---
# <span data-ttu-id="aabcd-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aabcd-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="aabcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aabcd-102">SYNOPSIS</span></span>
<span data-ttu-id="aabcd-103">Aktualisiert eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="aabcd-103">Updates a container registry.</span></span>

## <span data-ttu-id="aabcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aabcd-104">SYNTAX</span></span>

### <span data-ttu-id="aabcd-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aabcd-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aabcd-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aabcd-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aabcd-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aabcd-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aabcd-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aabcd-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aabcd-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aabcd-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aabcd-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aabcd-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aabcd-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aabcd-111">DESCRIPTION</span></span>
<span data-ttu-id="aabcd-112">Das Update-AzContainerRegistry aktualisiert eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="aabcd-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="aabcd-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aabcd-113">EXAMPLES</span></span>

### <span data-ttu-id="aabcd-114">Beispiel 1: Aktivieren des Administratorbenutzers für eine angegebene Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="aabcd-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="aabcd-115">Dieser Befehl aktiviert den Administratorbenutzer für die angegebene Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="aabcd-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="aabcd-116">Beispiel 2: Festlegen des von einer angegebenen Containerregistrierung verwendeten Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="aabcd-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="aabcd-117">Mit diesem Befehl wird die angegebene Containerregistrierung so festgelegt, dass ein vorhandenes Speicherkonto \` "mystorageaccount" \` im selben Abonnement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aabcd-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="aabcd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aabcd-118">PARAMETERS</span></span>

### <span data-ttu-id="aabcd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aabcd-119">-DefaultProfile</span></span>
<span data-ttu-id="aabcd-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aabcd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aabcd-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="aabcd-121">-DisableAdminUser</span></span>
<span data-ttu-id="aabcd-122">Aktivieren Sie den Administratorbenutzer für die Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="aabcd-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="aabcd-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="aabcd-123">-EnableAdminUser</span></span>
<span data-ttu-id="aabcd-124">Aktivieren Sie den Administratorbenutzer für die Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="aabcd-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="aabcd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="aabcd-125">-Name</span></span>
<span data-ttu-id="aabcd-126">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="aabcd-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="aabcd-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="aabcd-127">-NetworkRuleSet</span></span>
<span data-ttu-id="aabcd-128">Die für eine Containerregistrierung festgelegte Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="aabcd-128">The network rule set for a container registry.</span></span>

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

### <span data-ttu-id="aabcd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aabcd-129">-ResourceGroupName</span></span>
<span data-ttu-id="aabcd-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="aabcd-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="aabcd-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aabcd-131">-ResourceId</span></span>
<span data-ttu-id="aabcd-132">Die Containerregistrierungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="aabcd-132">The container registry resource id</span></span>

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

### <span data-ttu-id="aabcd-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="aabcd-133">-Sku</span></span>
<span data-ttu-id="aabcd-134">Containerregistrierungs-SKU.</span><span class="sxs-lookup"><span data-stu-id="aabcd-134">Container Registry SKU.</span></span>

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

### <span data-ttu-id="aabcd-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aabcd-135">-StorageAccountName</span></span>
<span data-ttu-id="aabcd-136">Der Name eines vorhandenen Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="aabcd-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="aabcd-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="aabcd-137">-Tag</span></span>
<span data-ttu-id="aabcd-138">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="aabcd-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="aabcd-139">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="aabcd-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="aabcd-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aabcd-140">-Confirm</span></span>
<span data-ttu-id="aabcd-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aabcd-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aabcd-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aabcd-142">-WhatIf</span></span>
<span data-ttu-id="aabcd-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aabcd-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aabcd-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aabcd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aabcd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aabcd-145">CommonParameters</span></span>
<span data-ttu-id="aabcd-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aabcd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aabcd-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aabcd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aabcd-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aabcd-148">INPUTS</span></span>

### <span data-ttu-id="aabcd-149">System.String</span><span class="sxs-lookup"><span data-stu-id="aabcd-149">System.String</span></span>

## <span data-ttu-id="aabcd-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aabcd-150">OUTPUTS</span></span>

### <span data-ttu-id="aabcd-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aabcd-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="aabcd-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aabcd-152">NOTES</span></span>

## <span data-ttu-id="aabcd-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aabcd-153">RELATED LINKS</span></span>

[<span data-ttu-id="aabcd-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aabcd-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="aabcd-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aabcd-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="aabcd-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aabcd-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

