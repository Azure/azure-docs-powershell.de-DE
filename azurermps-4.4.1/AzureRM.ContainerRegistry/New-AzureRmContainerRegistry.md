---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: 232d767130b789f61d7e4e21fa0bc7c0737c58dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479877"
---
# <span data-ttu-id="c2912-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2912-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="c2912-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2912-102">SYNOPSIS</span></span>
<span data-ttu-id="c2912-103">Erstellt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="c2912-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2912-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2912-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2912-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2912-105">DESCRIPTION</span></span>
<span data-ttu-id="c2912-106">Das Cmdlet **New-AzureRmContainerRegistry** erstellt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="c2912-106">The **New-AzureRmContainerRegistry** cmdlet creates a container registry.</span></span>

## <span data-ttu-id="c2912-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2912-107">EXAMPLES</span></span>

### <span data-ttu-id="c2912-108">Beispiel 1: Erstellen einer Container Registrierung mit einem neuen Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="c2912-108">Example 1: Create a container registry with a new storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

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
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

<span data-ttu-id="c2912-109">Mit diesem Befehl wird eine Container Registrierung mit einem neuen Speicherkonto in der Ressourcengruppe erstellt `MyResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="c2912-109">This command creates a container registry with a new storage account in the resource group `MyResourceGroup`.</span></span>

### <span data-ttu-id="c2912-110">Beispiel 2: Erstellen einer Container Registrierung mit aktiviertem Administrator Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c2912-110">Example 2: Create a container registry with admin user enabled.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

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

<span data-ttu-id="c2912-111">Mit diesem Befehl wird eine Container Registrierung mit aktiviertem Administrator Benutzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2912-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="c2912-112">Beispiel 3: Erstellen einer Container Registrierung mit einem vorhandenen Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="c2912-112">Example 3: Create a container registry with an existing storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

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
AdminUserEnabled   : False
StorageAccountName : mystorageaccount
```

<span data-ttu-id="c2912-113">Dieser Befehl erstellt eine Container Registrierung mit einem vorhandenen Speicherkonto `mystorageaccount` im gleichen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2912-113">This command creates a container registry with an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="c2912-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2912-114">PARAMETERS</span></span>

### <span data-ttu-id="c2912-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="c2912-115">-EnableAdminUser</span></span>
<span data-ttu-id="c2912-116">Aktivieren Sie den Administrator Benutzer für die Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="c2912-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2912-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="c2912-117">-Location</span></span>
<span data-ttu-id="c2912-118">Speicherort der Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="c2912-118">Container Registry Location.</span></span>
<span data-ttu-id="c2912-119">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2912-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="c2912-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c2912-120">-Name</span></span>
<span data-ttu-id="c2912-121">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="c2912-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="c2912-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2912-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2912-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2912-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="c2912-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="c2912-124">-Sku</span></span>
<span data-ttu-id="c2912-125">Container Registrierungs-SKU.</span><span class="sxs-lookup"><span data-stu-id="c2912-125">Container Registry SKU.</span></span>
<span data-ttu-id="c2912-126">Zulässige Werte: Basic.</span><span class="sxs-lookup"><span data-stu-id="c2912-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2912-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c2912-127">-StorageAccountName</span></span>
<span data-ttu-id="c2912-128">Der Name eines vorhandenen speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="c2912-128">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="c2912-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2912-129">-Tag</span></span>
<span data-ttu-id="c2912-130">Container Registrierungs Tags. Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="c2912-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c2912-131">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c2912-131">For example:</span></span>

<span data-ttu-id="c2912-132">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="c2912-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c2912-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2912-133">-Confirm</span></span>
<span data-ttu-id="c2912-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2912-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2912-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2912-135">-WhatIf</span></span>
<span data-ttu-id="c2912-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2912-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2912-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2912-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2912-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2912-138">-DefaultProfile</span></span>
<span data-ttu-id="c2912-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2912-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2912-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2912-140">CommonParameters</span></span>
<span data-ttu-id="c2912-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2912-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2912-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2912-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2912-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2912-143">INPUTS</span></span>

## <span data-ttu-id="c2912-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2912-144">OUTPUTS</span></span>

### <span data-ttu-id="c2912-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2912-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="c2912-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2912-146">NOTES</span></span>

## <span data-ttu-id="c2912-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2912-147">RELATED LINKS</span></span>

[<span data-ttu-id="c2912-148">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2912-148">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="c2912-149">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2912-149">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="c2912-150">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2912-150">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
