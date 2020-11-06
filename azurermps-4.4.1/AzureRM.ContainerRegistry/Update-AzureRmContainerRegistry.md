---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 5f59ae54d472d1d831b41f58789625c195961de5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503245"
---
# <span data-ttu-id="84625-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84625-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="84625-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84625-102">SYNOPSIS</span></span>
<span data-ttu-id="84625-103">Aktualisiert eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="84625-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84625-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84625-104">SYNTAX</span></span>

### <span data-ttu-id="84625-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="84625-105">Empty (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84625-106">EnableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="84625-106">EnableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84625-107">DisableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="84625-107">DisableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84625-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84625-108">DESCRIPTION</span></span>
<span data-ttu-id="84625-109">Das Cmdlet **Update-AzureRmContainerRegistry** aktualisiert eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="84625-109">The **Update-AzureRmContainerRegistry** cmdlet updates a container registry.</span></span>

## <span data-ttu-id="84625-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84625-110">EXAMPLES</span></span>

### <span data-ttu-id="84625-111">Beispiel 1: Aktivieren des Administratorbenutzers für eine bestimmte Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="84625-111">Example 1: Enable admin user for a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : myregistry154817
```

<span data-ttu-id="84625-112">Mit diesem Befehl wird Administrator Benutzer für die angegebene Container Registrierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="84625-112">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="84625-113">Beispiel 2: Einrichten des von einer bestimmten Container Registrierung verwendeten speicherkontos</span><span class="sxs-lookup"><span data-stu-id="84625-113">Example 2: Set the storage account used by a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : mystorageaccount
```

<span data-ttu-id="84625-114">Mit diesem Befehl wird die angegebene Container Registrierung so festgelegt, dass ein vorhandenes Speicherkonto `mystorageaccount` im gleichen Abonnement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84625-114">This command sets the specified container registry to use an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="84625-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="84625-115">PARAMETERS</span></span>

### <span data-ttu-id="84625-116">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="84625-116">-DisableAdminUser</span></span>
<span data-ttu-id="84625-117">Aktivieren Sie den Administrator Benutzer für die Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="84625-117">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: DisableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84625-118">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="84625-118">-EnableAdminUser</span></span>
<span data-ttu-id="84625-119">Aktivieren Sie den Administrator Benutzer für die Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="84625-119">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84625-120">-Name</span><span class="sxs-lookup"><span data-stu-id="84625-120">-Name</span></span>
<span data-ttu-id="84625-121">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="84625-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84625-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84625-122">-ResourceGroupName</span></span>
<span data-ttu-id="84625-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="84625-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="84625-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="84625-124">-StorageAccountName</span></span>
<span data-ttu-id="84625-125">Der Name eines vorhandenen speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="84625-125">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="84625-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="84625-126">-Tag</span></span>
<span data-ttu-id="84625-127">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="84625-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="84625-128">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="84625-128">For example:</span></span>

<span data-ttu-id="84625-129">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="84625-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="84625-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84625-130">-Confirm</span></span>
<span data-ttu-id="84625-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84625-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84625-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84625-132">-WhatIf</span></span>
<span data-ttu-id="84625-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84625-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84625-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84625-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84625-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84625-135">-DefaultProfile</span></span>
<span data-ttu-id="84625-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="84625-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84625-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84625-137">CommonParameters</span></span>
<span data-ttu-id="84625-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84625-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84625-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84625-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84625-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84625-140">INPUTS</span></span>

## <span data-ttu-id="84625-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84625-141">OUTPUTS</span></span>

### <span data-ttu-id="84625-142">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84625-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="84625-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="84625-143">NOTES</span></span>

## <span data-ttu-id="84625-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84625-144">RELATED LINKS</span></span>

[<span data-ttu-id="84625-145">Neu – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84625-145">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="84625-146">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84625-146">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="84625-147">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84625-147">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
