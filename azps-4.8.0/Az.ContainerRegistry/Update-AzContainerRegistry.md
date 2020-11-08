---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 606f92a3cc75deb40b3781b3578e38794ae65b2b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009285"
---
# <span data-ttu-id="152dd-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="152dd-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="152dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="152dd-102">SYNOPSIS</span></span>
<span data-ttu-id="152dd-103">Aktualisiert eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="152dd-103">Updates a container registry.</span></span>

## <span data-ttu-id="152dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="152dd-104">SYNTAX</span></span>

### <span data-ttu-id="152dd-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="152dd-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="152dd-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="152dd-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="152dd-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="152dd-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="152dd-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="152dd-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="152dd-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="152dd-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="152dd-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="152dd-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="152dd-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="152dd-111">DESCRIPTION</span></span>
<span data-ttu-id="152dd-112">Das Update-AzContainerRegistry-Cmdlet aktualisiert eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="152dd-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="152dd-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="152dd-113">EXAMPLES</span></span>

### <span data-ttu-id="152dd-114">Beispiel 1: Aktivieren des Administratorbenutzers für eine bestimmte Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="152dd-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="152dd-115">Mit diesem Befehl wird Administrator Benutzer für die angegebene Container Registrierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="152dd-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="152dd-116">Beispiel 2: Einrichten des von einer bestimmten Container Registrierung verwendeten speicherkontos</span><span class="sxs-lookup"><span data-stu-id="152dd-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="152dd-117">Mit diesem Befehl wird die angegebene Container Registrierung so festgelegt, dass eine vorhandene Speicherkonto \` \` -mystorageaccount im gleichen Abonnement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="152dd-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="152dd-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="152dd-118">PARAMETERS</span></span>

### <span data-ttu-id="152dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="152dd-119">-DefaultProfile</span></span>
<span data-ttu-id="152dd-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="152dd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="152dd-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="152dd-121">-DisableAdminUser</span></span>
<span data-ttu-id="152dd-122">Aktivieren Sie den Administrator Benutzer für die Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="152dd-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="152dd-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="152dd-123">-EnableAdminUser</span></span>
<span data-ttu-id="152dd-124">Aktivieren Sie den Administrator Benutzer für die Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="152dd-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="152dd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="152dd-125">-Name</span></span>
<span data-ttu-id="152dd-126">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="152dd-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="152dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="152dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="152dd-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="152dd-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="152dd-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="152dd-129">-ResourceId</span></span>
<span data-ttu-id="152dd-130">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="152dd-130">The container registry resource id</span></span>

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

### <span data-ttu-id="152dd-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="152dd-131">-Sku</span></span>
<span data-ttu-id="152dd-132">Container Registrierungs-SKU.</span><span class="sxs-lookup"><span data-stu-id="152dd-132">Container Registry SKU.</span></span>

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

### <span data-ttu-id="152dd-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="152dd-133">-StorageAccountName</span></span>
<span data-ttu-id="152dd-134">Der Name eines vorhandenen speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="152dd-134">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="152dd-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="152dd-135">-Tag</span></span>
<span data-ttu-id="152dd-136">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="152dd-136">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="152dd-137">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="152dd-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="152dd-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="152dd-138">-Confirm</span></span>
<span data-ttu-id="152dd-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="152dd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="152dd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="152dd-140">-WhatIf</span></span>
<span data-ttu-id="152dd-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="152dd-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="152dd-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="152dd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="152dd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152dd-143">CommonParameters</span></span>
<span data-ttu-id="152dd-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="152dd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152dd-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="152dd-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152dd-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="152dd-146">INPUTS</span></span>

### <span data-ttu-id="152dd-147">System. String</span><span class="sxs-lookup"><span data-stu-id="152dd-147">System.String</span></span>

## <span data-ttu-id="152dd-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="152dd-148">OUTPUTS</span></span>

### <span data-ttu-id="152dd-149">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="152dd-149">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="152dd-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="152dd-150">NOTES</span></span>

## <span data-ttu-id="152dd-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="152dd-151">RELATED LINKS</span></span>

[<span data-ttu-id="152dd-152">Neu – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="152dd-152">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="152dd-153">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="152dd-153">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="152dd-154">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="152dd-154">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

