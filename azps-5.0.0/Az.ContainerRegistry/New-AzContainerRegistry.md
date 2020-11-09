---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296386"
---
# <span data-ttu-id="ae8e7-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae8e7-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="ae8e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ae8e7-103">Erstellt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-103">Creates a container registry.</span></span>

## <span data-ttu-id="ae8e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae8e7-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae8e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae8e7-105">DESCRIPTION</span></span>
<span data-ttu-id="ae8e7-106">Das New-AzContainerRegistry-Cmdlet erstellt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="ae8e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae8e7-107">EXAMPLES</span></span>

### <span data-ttu-id="ae8e7-108">Beispiel 1: Erstellen einer Container Registrierung mit einem neuen Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="ae8e7-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="ae8e7-109">Mit diesem Befehl wird eine Container Registrierung mit einem neuen Speicherkonto in der Ressourcengruppe \` myresourcegroup erstellt \` .</span><span class="sxs-lookup"><span data-stu-id="ae8e7-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="ae8e7-110">Beispiel 2: Erstellen einer Container Registrierung mit aktiviertem Administrator Benutzer.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="ae8e7-111">Mit diesem Befehl wird eine Container Registrierung mit aktiviertem Administrator Benutzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="ae8e7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae8e7-112">PARAMETERS</span></span>

### <span data-ttu-id="ae8e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae8e7-113">-DefaultProfile</span></span>
<span data-ttu-id="ae8e7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ae8e7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae8e7-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="ae8e7-115">-EnableAdminUser</span></span>
<span data-ttu-id="ae8e7-116">Aktivieren Sie den Administrator Benutzer für die Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8e7-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="ae8e7-117">-Location</span></span>
<span data-ttu-id="ae8e7-118">Speicherort der Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-118">Container Registry Location.</span></span>
<span data-ttu-id="ae8e7-119">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="ae8e7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ae8e7-120">-Name</span></span>
<span data-ttu-id="ae8e7-121">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="ae8e7-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="ae8e7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae8e7-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae8e7-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="ae8e7-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="ae8e7-124">-Sku</span></span>
<span data-ttu-id="ae8e7-125">Container Registrierungs-SKU.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-125">Container Registry SKU.</span></span>
<span data-ttu-id="ae8e7-126">Zulässige Werte: Basic.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8e7-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae8e7-127">-Tag</span></span>
<span data-ttu-id="ae8e7-128">Container Registrierungs Tags. Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="ae8e7-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="ae8e7-129">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="ae8e7-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ae8e7-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ae8e7-130">-Confirm</span></span>
<span data-ttu-id="ae8e7-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae8e7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae8e7-132">-WhatIf</span></span>
<span data-ttu-id="ae8e7-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae8e7-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae8e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae8e7-135">CommonParameters</span></span>
<span data-ttu-id="ae8e7-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae8e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae8e7-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae8e7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae8e7-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae8e7-138">INPUTS</span></span>

### <span data-ttu-id="ae8e7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ae8e7-139">System.String</span></span>

## <span data-ttu-id="ae8e7-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae8e7-140">OUTPUTS</span></span>

### <span data-ttu-id="ae8e7-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae8e7-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="ae8e7-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae8e7-142">NOTES</span></span>

## <span data-ttu-id="ae8e7-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae8e7-143">RELATED LINKS</span></span>

[<span data-ttu-id="ae8e7-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae8e7-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="ae8e7-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae8e7-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="ae8e7-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae8e7-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

