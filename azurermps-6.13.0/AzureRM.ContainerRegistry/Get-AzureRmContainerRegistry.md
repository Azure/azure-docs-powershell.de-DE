---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: 3d9580549308c17c92037b3e31a337f11bbe6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476169"
---
# <span data-ttu-id="ddb0d-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ddb0d-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="ddb0d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ddb0d-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb0d-103">Ruft eine Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="ddb0d-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddb0d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddb0d-104">SYNTAX</span></span>

### <span data-ttu-id="ddb0d-105">ListRegistriesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ddb0d-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddb0d-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddb0d-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddb0d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddb0d-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ddb0d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ddb0d-108">DESCRIPTION</span></span>
<span data-ttu-id="ddb0d-109">Das Get-AzureRmContainerRegistry-Cmdlet ruft eine angegebene Container Registrierung oder alle Container Register in einer Ressourcengruppe oder dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="ddb0d-109">The Get-AzureRmContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="ddb0d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ddb0d-110">EXAMPLES</span></span>

### <span data-ttu-id="ddb0d-111">Beispiel 1: Abrufen einer angegebenen Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="ddb0d-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="ddb0d-112">Dieser Befehl ruft die angegebene Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="ddb0d-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="ddb0d-113">Beispiel 2: Abrufen aller Container Register in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ddb0d-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

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

<span data-ttu-id="ddb0d-114">Dieser Befehl ruft alle Container Register in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ddb0d-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="ddb0d-115">Beispiel 3: Abrufen aller Container Register im Abonnement</span><span class="sxs-lookup"><span data-stu-id="ddb0d-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry

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

<span data-ttu-id="ddb0d-116">Dieser Befehl ruft alle Container Register im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="ddb0d-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="ddb0d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddb0d-117">PARAMETERS</span></span>

### <span data-ttu-id="ddb0d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb0d-118">-DefaultProfile</span></span>
<span data-ttu-id="ddb0d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ddb0d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddb0d-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="ddb0d-120">-IncludeDetail</span></span>
<span data-ttu-id="ddb0d-121">Zeigen Sie weitere Details zur Container Registrierung an.</span><span class="sxs-lookup"><span data-stu-id="ddb0d-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="ddb0d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ddb0d-122">-Name</span></span>
<span data-ttu-id="ddb0d-123">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="ddb0d-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="ddb0d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb0d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ddb0d-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ddb0d-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ddb0d-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ddb0d-126">-ResourceId</span></span>
<span data-ttu-id="ddb0d-127">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="ddb0d-127">The container registry resource id</span></span>

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

### <span data-ttu-id="ddb0d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb0d-128">CommonParameters</span></span>
<span data-ttu-id="ddb0d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddb0d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb0d-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddb0d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb0d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ddb0d-131">INPUTS</span></span>

### <span data-ttu-id="ddb0d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ddb0d-132">System.String</span></span>

## <span data-ttu-id="ddb0d-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ddb0d-133">OUTPUTS</span></span>

### <span data-ttu-id="ddb0d-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ddb0d-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="ddb0d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="ddb0d-135">NOTES</span></span>

## <span data-ttu-id="ddb0d-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ddb0d-136">RELATED LINKS</span></span>

[<span data-ttu-id="ddb0d-137">Neu – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ddb0d-137">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="ddb0d-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ddb0d-138">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="ddb0d-139">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ddb0d-139">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

