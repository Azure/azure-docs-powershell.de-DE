---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 969e37173c487b2ed3ee4ab6dad5374208f5ff27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945256"
---
# <span data-ttu-id="af7cc-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af7cc-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="af7cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af7cc-102">SYNOPSIS</span></span>
<span data-ttu-id="af7cc-103">Ruft eine Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="af7cc-103">Gets a container registry.</span></span>

## <span data-ttu-id="af7cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af7cc-104">SYNTAX</span></span>

### <span data-ttu-id="af7cc-105">ListRegistriesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="af7cc-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af7cc-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af7cc-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af7cc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af7cc-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af7cc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af7cc-108">DESCRIPTION</span></span>
<span data-ttu-id="af7cc-109">Das Get-AzContainerRegistry-Cmdlet ruft eine angegebene Containerregistrierung oder alle Containerregistrierungsstellen in einer Ressourcengruppe oder im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="af7cc-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="af7cc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af7cc-110">EXAMPLES</span></span>

### <span data-ttu-id="af7cc-111">Beispiel 1: Erhalten einer angegebenen Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="af7cc-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="af7cc-112">Dieser Befehl ruft die angegebene Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="af7cc-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="af7cc-113">Beispiel 2: Alle Containerregistrierungsstellen in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="af7cc-113">Example 2: Get all the container registries in a resource group</span></span>
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

<span data-ttu-id="af7cc-114">Dieser Befehl ruft alle Containerregistrierungsstellen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="af7cc-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="af7cc-115">Beispiel 3: Alle Containerregistrierungsstellen im Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="af7cc-115">Example 3:  Get all the container registries in the subscription</span></span>
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

<span data-ttu-id="af7cc-116">Dieser Befehl ruft alle Containerregistrierungsstellen im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="af7cc-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="af7cc-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="af7cc-117">PARAMETERS</span></span>

### <span data-ttu-id="af7cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7cc-118">-DefaultProfile</span></span>
<span data-ttu-id="af7cc-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="af7cc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af7cc-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="af7cc-120">-IncludeDetail</span></span>
<span data-ttu-id="af7cc-121">Weitere Details zur Containerregistrierung anzeigen</span><span class="sxs-lookup"><span data-stu-id="af7cc-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="af7cc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="af7cc-122">-Name</span></span>
<span data-ttu-id="af7cc-123">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="af7cc-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="af7cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af7cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="af7cc-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="af7cc-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="af7cc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af7cc-126">-ResourceId</span></span>
<span data-ttu-id="af7cc-127">Die Containerregistrierungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="af7cc-127">The container registry resource id</span></span>

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

### <span data-ttu-id="af7cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7cc-128">CommonParameters</span></span>
<span data-ttu-id="af7cc-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af7cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7cc-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af7cc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7cc-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af7cc-131">INPUTS</span></span>

### <span data-ttu-id="af7cc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="af7cc-132">System.String</span></span>

## <span data-ttu-id="af7cc-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af7cc-133">OUTPUTS</span></span>

### <span data-ttu-id="af7cc-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af7cc-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="af7cc-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="af7cc-135">NOTES</span></span>

## <span data-ttu-id="af7cc-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="af7cc-136">RELATED LINKS</span></span>

[<span data-ttu-id="af7cc-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af7cc-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="af7cc-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af7cc-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="af7cc-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af7cc-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

