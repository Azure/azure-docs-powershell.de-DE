---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: dc1b35831de68ad31877be05610d1b075b27452f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503809"
---
# <span data-ttu-id="26000-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="26000-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="26000-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26000-102">SYNOPSIS</span></span>
<span data-ttu-id="26000-103">Ruft eine Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="26000-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26000-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26000-104">SYNTAX</span></span>

### <span data-ttu-id="26000-105">ListRegistriesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="26000-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26000-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="26000-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26000-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26000-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26000-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26000-108">DESCRIPTION</span></span>
<span data-ttu-id="26000-109">Das Get-AzureRmContainerRegistry-Cmdlet ruft eine angegebene Container Registrierung oder alle Container Register in einer Ressourcengruppe oder dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="26000-109">The Get-AzureRmContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="26000-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26000-110">EXAMPLES</span></span>

### <span data-ttu-id="26000-111">Beispiel 1: Abrufen einer angegebenen Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="26000-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="26000-112">Dieser Befehl ruft die angegebene Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="26000-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="26000-113">Beispiel 2: Abrufen aller Container Register in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="26000-113">Example 2: Get all the container registries in a resource group</span></span>
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

<span data-ttu-id="26000-114">Dieser Befehl ruft alle Container Register in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="26000-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="26000-115">Beispiel 3: Abrufen aller Container Register im Abonnement</span><span class="sxs-lookup"><span data-stu-id="26000-115">Example 3:  Get all the container registries in the subscription</span></span>
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

<span data-ttu-id="26000-116">Dieser Befehl ruft alle Container Register im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="26000-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="26000-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="26000-117">PARAMETERS</span></span>

### <span data-ttu-id="26000-118">-Name</span><span class="sxs-lookup"><span data-stu-id="26000-118">-Name</span></span>
<span data-ttu-id="26000-119">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="26000-119">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26000-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26000-120">-ResourceGroupName</span></span>
<span data-ttu-id="26000-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="26000-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListRegistriesParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RegistryNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26000-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26000-122">-DefaultProfile</span></span>
<span data-ttu-id="26000-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="26000-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26000-124">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="26000-124">-IncludeDetail</span></span>
<span data-ttu-id="26000-125">Zeigen Sie weitere Details zur Container Registrierung an.</span><span class="sxs-lookup"><span data-stu-id="26000-125">Show more details about the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26000-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="26000-126">-ResourceId</span></span>
<span data-ttu-id="26000-127">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="26000-127">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26000-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26000-128">CommonParameters</span></span>
<span data-ttu-id="26000-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26000-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26000-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26000-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26000-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26000-131">INPUTS</span></span>

### <span data-ttu-id="26000-132">Keine</span><span class="sxs-lookup"><span data-stu-id="26000-132">None</span></span>
<span data-ttu-id="26000-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="26000-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26000-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26000-134">OUTPUTS</span></span>

### <span data-ttu-id="26000-135">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="26000-135">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="26000-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="26000-136">NOTES</span></span>

## <span data-ttu-id="26000-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26000-137">RELATED LINKS</span></span>

[<span data-ttu-id="26000-138">Neu – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="26000-138">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="26000-139">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="26000-139">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="26000-140">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="26000-140">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

