---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 759bc79a7ab36f99e01ce1e96b0bb6c3c6a9483b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148716"
---
# <span data-ttu-id="25ae9-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="25ae9-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="25ae9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="25ae9-103">Ruft eine Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="25ae9-103">Gets a container registry.</span></span>

## <span data-ttu-id="25ae9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25ae9-104">SYNTAX</span></span>

### <span data-ttu-id="25ae9-105">ListRegistriesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="25ae9-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25ae9-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25ae9-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25ae9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25ae9-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25ae9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25ae9-108">DESCRIPTION</span></span>
<span data-ttu-id="25ae9-109">Das Get-AzContainerRegistry ruft eine angegebene Containerregistrierung oder alle Containerregistrierungen in einer Ressourcengruppe oder im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="25ae9-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="25ae9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25ae9-110">EXAMPLES</span></span>

### <span data-ttu-id="25ae9-111">Beispiel 1: Erhalten einer angegebenen Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="25ae9-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="25ae9-112">Dieser Befehl ruft die angegebene Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="25ae9-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="25ae9-113">Beispiel 2: Alle Containerregistrierungen in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="25ae9-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="25ae9-114">Dieser Befehl ruft alle Containerregistrierungen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="25ae9-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="25ae9-115">Beispiel 3: Alle Containerregistrierungen im Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="25ae9-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzContainerRegistry

  Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="25ae9-116">Dieser Befehl ruft alle Containerregistrierungen im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="25ae9-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="25ae9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25ae9-117">PARAMETERS</span></span>

### <span data-ttu-id="25ae9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ae9-118">-DefaultProfile</span></span>
<span data-ttu-id="25ae9-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="25ae9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25ae9-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="25ae9-120">-IncludeDetail</span></span>
<span data-ttu-id="25ae9-121">Zeigen Sie weitere Details zur Containerregistrierung an.</span><span class="sxs-lookup"><span data-stu-id="25ae9-121">Show more details about the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25ae9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="25ae9-122">-Name</span></span>
<span data-ttu-id="25ae9-123">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="25ae9-123">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ae9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25ae9-124">-ResourceGroupName</span></span>
<span data-ttu-id="25ae9-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="25ae9-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListRegistriesParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ae9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25ae9-126">-ResourceId</span></span>
<span data-ttu-id="25ae9-127">Die Containerregistrierungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="25ae9-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ae9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ae9-128">CommonParameters</span></span>
<span data-ttu-id="25ae9-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25ae9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ae9-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25ae9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ae9-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25ae9-131">INPUTS</span></span>

### <span data-ttu-id="25ae9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="25ae9-132">System.String</span></span>

## <span data-ttu-id="25ae9-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25ae9-133">OUTPUTS</span></span>

### <span data-ttu-id="25ae9-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="25ae9-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="25ae9-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25ae9-135">NOTES</span></span>

## <span data-ttu-id="25ae9-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25ae9-136">RELATED LINKS</span></span>

[<span data-ttu-id="25ae9-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="25ae9-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="25ae9-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="25ae9-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="25ae9-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="25ae9-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

