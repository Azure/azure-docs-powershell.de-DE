---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: ce72af78fec87182e1061259cd0c0d51d9819767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478554"
---
# <span data-ttu-id="d777d-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d777d-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="d777d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d777d-102">SYNOPSIS</span></span>
<span data-ttu-id="d777d-103">Erstellt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d777d-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d777d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d777d-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d777d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d777d-105">DESCRIPTION</span></span>
<span data-ttu-id="d777d-106">Das New-AzureRmContainerRegistry-Cmdlet erstellt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d777d-106">The New-AzureRmContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="d777d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d777d-107">EXAMPLES</span></span>

### <span data-ttu-id="d777d-108">Beispiel 1: Erstellen einer Container Registrierung mit einem neuen Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="d777d-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="d777d-109">Mit diesem Befehl wird eine Container Registrierung mit einem neuen Speicherkonto in der Ressourcengruppe \` myresourcegroup erstellt \` .</span><span class="sxs-lookup"><span data-stu-id="d777d-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="d777d-110">Beispiel 2: Erstellen einer Container Registrierung mit aktiviertem Administrator Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d777d-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="d777d-111">Mit diesem Befehl wird eine Container Registrierung mit aktiviertem Administrator Benutzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="d777d-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="d777d-112">Beispiel 3: Erstellen einer Container Registrierung mit einem vorhandenen Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="d777d-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="d777d-113">Dieser Befehl erstellt eine Container Registrierung mit einem vorhandenen Speicherkonto \` mystorageaccount \` im gleichen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d777d-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="d777d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d777d-114">PARAMETERS</span></span>

### <span data-ttu-id="d777d-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="d777d-115">-EnableAdminUser</span></span>
<span data-ttu-id="d777d-116">Aktivieren Sie den Administrator Benutzer für die Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d777d-116">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777d-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="d777d-117">-Location</span></span>
<span data-ttu-id="d777d-118">Speicherort der Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d777d-118">Container Registry Location.</span></span>
<span data-ttu-id="d777d-119">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="d777d-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="d777d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d777d-120">-Name</span></span>
<span data-ttu-id="d777d-121">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="d777d-121">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d777d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d777d-122">-ResourceGroupName</span></span>
<span data-ttu-id="d777d-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d777d-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="d777d-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="d777d-124">-Sku</span></span>
<span data-ttu-id="d777d-125">Container Registrierungs-SKU.</span><span class="sxs-lookup"><span data-stu-id="d777d-125">Container Registry SKU.</span></span>
<span data-ttu-id="d777d-126">Zulässige Werte: Basic.</span><span class="sxs-lookup"><span data-stu-id="d777d-126">Allowed values: Basic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777d-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d777d-127">-StorageAccountName</span></span>
<span data-ttu-id="d777d-128">Der Name eines vorhandenen speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="d777d-128">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="d777d-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="d777d-129">-Tag</span></span>
<span data-ttu-id="d777d-130">Container Registrierungs Tags. Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="d777d-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="d777d-131">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d777d-131">For example:</span></span>

<span data-ttu-id="d777d-132">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="d777d-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777d-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d777d-133">-Confirm</span></span>
<span data-ttu-id="d777d-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d777d-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d777d-135">-WhatIf</span></span>
<span data-ttu-id="d777d-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d777d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d777d-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d777d-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777d-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d777d-138">-DefaultProfile</span></span>
<span data-ttu-id="d777d-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d777d-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d777d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d777d-140">CommonParameters</span></span>
<span data-ttu-id="d777d-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d777d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d777d-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d777d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d777d-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d777d-143">INPUTS</span></span>

### <span data-ttu-id="d777d-144">Keine</span><span class="sxs-lookup"><span data-stu-id="d777d-144">None</span></span>
<span data-ttu-id="d777d-145">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d777d-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d777d-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d777d-146">OUTPUTS</span></span>

### <span data-ttu-id="d777d-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d777d-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="d777d-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="d777d-148">NOTES</span></span>

## <span data-ttu-id="d777d-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d777d-149">RELATED LINKS</span></span>

[<span data-ttu-id="d777d-150">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d777d-150">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="d777d-151">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d777d-151">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="d777d-152">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d777d-152">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

