---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: fc9d8db7f293ff94e33b50afd55176d157046fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499165"
---
# <span data-ttu-id="24329-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="24329-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="24329-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24329-102">SYNOPSIS</span></span>
<span data-ttu-id="24329-103">Ruft die Anmeldeinformationen für eine Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="24329-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24329-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24329-104">SYNTAX</span></span>

### <span data-ttu-id="24329-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="24329-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24329-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24329-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24329-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24329-107">DESCRIPTION</span></span>
<span data-ttu-id="24329-108">Das Cmdlet " **Get-AzureRmContainerRegistryCredential** " Ruft die Anmeldeinformationen für eine Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="24329-108">The **Get-AzureRmContainerRegistryCredential** cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="24329-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24329-109">EXAMPLES</span></span>

### <span data-ttu-id="24329-110">Beispiel 1: Abrufen der Anmeldeinformationen für eine Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="24329-110">Example 1: Get the login credentials for a container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="24329-111">Dieser Befehl ruft die Anmeldeinformationen für die angegebene Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="24329-111">This command gets the login credentials for the specified container registry.</span></span> <span data-ttu-id="24329-112">Der Administrator muss für die Container Registrierung aktiviert sein `MyRegistry` , um Anmeldeinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="24329-112">Admin user has to be enabled for the container registry `MyRegistry` to get login credentials.</span></span>

## <span data-ttu-id="24329-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="24329-113">PARAMETERS</span></span>

### <span data-ttu-id="24329-114">-Name</span><span class="sxs-lookup"><span data-stu-id="24329-114">-Name</span></span>
<span data-ttu-id="24329-115">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="24329-115">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24329-116">-Registry</span><span class="sxs-lookup"><span data-stu-id="24329-116">-Registry</span></span>
<span data-ttu-id="24329-117">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="24329-117">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24329-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24329-118">-ResourceGroupName</span></span>
<span data-ttu-id="24329-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="24329-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24329-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24329-120">-DefaultProfile</span></span>
<span data-ttu-id="24329-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24329-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24329-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24329-122">CommonParameters</span></span>
<span data-ttu-id="24329-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24329-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24329-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24329-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24329-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24329-125">INPUTS</span></span>

### <span data-ttu-id="24329-126">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="24329-126">PSContainerRegistry</span></span>
<span data-ttu-id="24329-127">Der Parameter "Registry" akzeptiert den Wert vom Typ "PSContainerRegistry" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="24329-127">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="24329-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24329-128">OUTPUTS</span></span>

### <span data-ttu-id="24329-129">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="24329-129">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="24329-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="24329-130">NOTES</span></span>

## <span data-ttu-id="24329-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24329-131">RELATED LINKS</span></span>

[<span data-ttu-id="24329-132">Neu – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="24329-132">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="24329-133">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="24329-133">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="24329-134">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="24329-134">Update-AzureRmContainerRegistryCredential</span></span>](./Update-AzureRmContainerRegistryCredential.md)

