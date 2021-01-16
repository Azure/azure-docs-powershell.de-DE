---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293404"
---
# <span data-ttu-id="fe889-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe889-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="fe889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe889-102">SYNOPSIS</span></span>
<span data-ttu-id="fe889-103">Aktualisiert eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="fe889-103">Updates a container registry.</span></span>

## <span data-ttu-id="fe889-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe889-104">SYNTAX</span></span>

### <span data-ttu-id="fe889-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe889-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe889-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe889-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe889-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe889-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe889-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe889-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe889-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe889-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe889-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe889-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe889-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe889-111">DESCRIPTION</span></span>
<span data-ttu-id="fe889-112">Das Update-AzContainerRegistry aktualisiert eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="fe889-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="fe889-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe889-113">EXAMPLES</span></span>

### <span data-ttu-id="fe889-114">Beispiel 1: Aktivieren des Administratorbenutzers für eine angegebene Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="fe889-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="fe889-115">Dieser Befehl aktiviert den Administratorbenutzer für die angegebene Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="fe889-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="fe889-116">Beispiel 2: Festlegen des von einer angegebenen Containerregistrierung verwendeten Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="fe889-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="fe889-117">Mit diesem Befehl wird die angegebene Containerregistrierung so festgelegt, dass ein vorhandenes Speicherkonto \` "mystorageaccount" \` im selben Abonnement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe889-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="fe889-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe889-118">PARAMETERS</span></span>

### <span data-ttu-id="fe889-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe889-119">-DefaultProfile</span></span>
<span data-ttu-id="fe889-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fe889-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe889-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="fe889-121">-DisableAdminUser</span></span>
<span data-ttu-id="fe889-122">Aktivieren Sie den Administratorbenutzer für die Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="fe889-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="fe889-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="fe889-123">-EnableAdminUser</span></span>
<span data-ttu-id="fe889-124">Aktivieren Sie den Administratorbenutzer für die Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="fe889-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="fe889-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fe889-125">-Name</span></span>
<span data-ttu-id="fe889-126">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="fe889-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="fe889-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe889-127">-NetworkRuleSet</span></span>
<span data-ttu-id="fe889-128">Die für eine Containerregistrierung festgelegte Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="fe889-128">The network rule set for a container registry.</span></span>

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

### <span data-ttu-id="fe889-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe889-129">-ResourceGroupName</span></span>
<span data-ttu-id="fe889-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="fe889-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="fe889-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe889-131">-ResourceId</span></span>
<span data-ttu-id="fe889-132">Die Containerregistrierungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fe889-132">The container registry resource id</span></span>

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

### <span data-ttu-id="fe889-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="fe889-133">-Sku</span></span>
<span data-ttu-id="fe889-134">Containerregistrierungs-SKU.</span><span class="sxs-lookup"><span data-stu-id="fe889-134">Container Registry SKU.</span></span>

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

### <span data-ttu-id="fe889-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fe889-135">-StorageAccountName</span></span>
<span data-ttu-id="fe889-136">Der Name eines vorhandenen Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="fe889-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="fe889-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe889-137">-Tag</span></span>
<span data-ttu-id="fe889-138">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="fe889-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="fe889-139">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="fe889-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fe889-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe889-140">-Confirm</span></span>
<span data-ttu-id="fe889-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe889-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe889-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fe889-142">-WhatIf</span></span>
<span data-ttu-id="fe889-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe889-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe889-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe889-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe889-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe889-145">CommonParameters</span></span>
<span data-ttu-id="fe889-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe889-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe889-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe889-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe889-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe889-148">INPUTS</span></span>

### <span data-ttu-id="fe889-149">System.String</span><span class="sxs-lookup"><span data-stu-id="fe889-149">System.String</span></span>

## <span data-ttu-id="fe889-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe889-150">OUTPUTS</span></span>

### <span data-ttu-id="fe889-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe889-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="fe889-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fe889-152">NOTES</span></span>

## <span data-ttu-id="fe889-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fe889-153">RELATED LINKS</span></span>

[<span data-ttu-id="fe889-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe889-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="fe889-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe889-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="fe889-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe889-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

