---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305112"
---
# <span data-ttu-id="87ea6-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="87ea6-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="87ea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="87ea6-103">Erstellt eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="87ea6-103">Creates a container registry.</span></span>

## <span data-ttu-id="87ea6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87ea6-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87ea6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87ea6-105">DESCRIPTION</span></span>
<span data-ttu-id="87ea6-106">Das New-AzContainerRegistry erstellt eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="87ea6-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="87ea6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87ea6-107">EXAMPLES</span></span>

### <span data-ttu-id="87ea6-108">Beispiel 1: Erstellen einer Containerregistrierung mit einem neuen Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="87ea6-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="87ea6-109">Mit diesem Befehl wird eine Containerregistrierung mit einem neuen Speicherkonto in der Ressourcengruppe \` "MyResourceGroup" \` erstellt.</span><span class="sxs-lookup"><span data-stu-id="87ea6-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="87ea6-110">Beispiel 2: Erstellen einer Containerregistrierung mit aktivierten Administratorbenutzern</span><span class="sxs-lookup"><span data-stu-id="87ea6-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="87ea6-111">Dieser Befehl erstellt eine Containerregistrierung mit aktivierten Administratorbenutzern.</span><span class="sxs-lookup"><span data-stu-id="87ea6-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="87ea6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87ea6-112">PARAMETERS</span></span>

### <span data-ttu-id="87ea6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ea6-113">-DefaultProfile</span></span>
<span data-ttu-id="87ea6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="87ea6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87ea6-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="87ea6-115">-EnableAdminUser</span></span>
<span data-ttu-id="87ea6-116">Aktivieren Sie den Administratorbenutzer für die Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="87ea6-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="87ea6-117">-Location</span><span class="sxs-lookup"><span data-stu-id="87ea6-117">-Location</span></span>
<span data-ttu-id="87ea6-118">Container Registry Location.</span><span class="sxs-lookup"><span data-stu-id="87ea6-118">Container Registry Location.</span></span>
<span data-ttu-id="87ea6-119">Standard für den Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="87ea6-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="87ea6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="87ea6-120">-Name</span></span>
<span data-ttu-id="87ea6-121">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="87ea6-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="87ea6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87ea6-122">-ResourceGroupName</span></span>
<span data-ttu-id="87ea6-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="87ea6-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="87ea6-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="87ea6-124">-Sku</span></span>
<span data-ttu-id="87ea6-125">Containerregistrierungs-SKU.</span><span class="sxs-lookup"><span data-stu-id="87ea6-125">Container Registry SKU.</span></span>
<span data-ttu-id="87ea6-126">Zulässige Werte: Standard.</span><span class="sxs-lookup"><span data-stu-id="87ea6-126">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="87ea6-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="87ea6-127">-Tag</span></span>
<span data-ttu-id="87ea6-128">Container Registry Tags.Key-value-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="87ea6-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="87ea6-129">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="87ea6-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="87ea6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87ea6-130">-Confirm</span></span>
<span data-ttu-id="87ea6-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87ea6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87ea6-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="87ea6-132">-WhatIf</span></span>
<span data-ttu-id="87ea6-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87ea6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87ea6-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87ea6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87ea6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ea6-135">CommonParameters</span></span>
<span data-ttu-id="87ea6-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87ea6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ea6-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87ea6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ea6-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87ea6-138">INPUTS</span></span>

### <span data-ttu-id="87ea6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="87ea6-139">System.String</span></span>

## <span data-ttu-id="87ea6-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87ea6-140">OUTPUTS</span></span>

### <span data-ttu-id="87ea6-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="87ea6-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="87ea6-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="87ea6-142">NOTES</span></span>

## <span data-ttu-id="87ea6-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="87ea6-143">RELATED LINKS</span></span>

[<span data-ttu-id="87ea6-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="87ea6-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="87ea6-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="87ea6-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="87ea6-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="87ea6-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

