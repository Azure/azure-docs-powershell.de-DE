---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 759bc79a7ab36f99e01ce1e96b0bb6c3c6a9483b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009979"
---
# <span data-ttu-id="1f840-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1f840-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="1f840-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f840-102">SYNOPSIS</span></span>
<span data-ttu-id="1f840-103">Ruft eine Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="1f840-103">Gets a container registry.</span></span>

## <span data-ttu-id="1f840-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f840-104">SYNTAX</span></span>

### <span data-ttu-id="1f840-105">ListRegistriesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f840-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f840-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f840-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f840-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f840-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f840-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f840-108">DESCRIPTION</span></span>
<span data-ttu-id="1f840-109">Das Get-AzContainerRegistry-Cmdlet ruft eine angegebene Container Registrierung oder alle Container Register in einer Ressourcengruppe oder dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="1f840-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="1f840-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f840-110">EXAMPLES</span></span>

### <span data-ttu-id="1f840-111">Beispiel 1: Abrufen einer angegebenen Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="1f840-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="1f840-112">Dieser Befehl ruft die angegebene Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="1f840-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="1f840-113">Beispiel 2: Abrufen aller Container Register in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1f840-113">Example 2: Get all the container registries in a resource group</span></span>
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

<span data-ttu-id="1f840-114">Dieser Befehl ruft alle Container Register in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="1f840-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="1f840-115">Beispiel 3: Abrufen aller Container Register im Abonnement</span><span class="sxs-lookup"><span data-stu-id="1f840-115">Example 3:  Get all the container registries in the subscription</span></span>
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

<span data-ttu-id="1f840-116">Dieser Befehl ruft alle Container Register im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="1f840-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="1f840-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f840-117">PARAMETERS</span></span>

### <span data-ttu-id="1f840-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f840-118">-DefaultProfile</span></span>
<span data-ttu-id="1f840-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1f840-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f840-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="1f840-120">-IncludeDetail</span></span>
<span data-ttu-id="1f840-121">Zeigen Sie weitere Details zur Container Registrierung an.</span><span class="sxs-lookup"><span data-stu-id="1f840-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="1f840-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1f840-122">-Name</span></span>
<span data-ttu-id="1f840-123">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="1f840-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="1f840-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f840-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f840-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1f840-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1f840-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1f840-126">-ResourceId</span></span>
<span data-ttu-id="1f840-127">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="1f840-127">The container registry resource id</span></span>

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

### <span data-ttu-id="1f840-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f840-128">CommonParameters</span></span>
<span data-ttu-id="1f840-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f840-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f840-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f840-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f840-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f840-131">INPUTS</span></span>

### <span data-ttu-id="1f840-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1f840-132">System.String</span></span>

## <span data-ttu-id="1f840-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f840-133">OUTPUTS</span></span>

### <span data-ttu-id="1f840-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1f840-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="1f840-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f840-135">NOTES</span></span>

## <span data-ttu-id="1f840-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f840-136">RELATED LINKS</span></span>

[<span data-ttu-id="1f840-137">Neu – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1f840-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="1f840-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1f840-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="1f840-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1f840-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

