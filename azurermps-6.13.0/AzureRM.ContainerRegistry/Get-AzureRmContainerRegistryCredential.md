---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 37ca6fad019814c476f48d1f086a430db75afb99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476166"
---
# <span data-ttu-id="bcc92-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="bcc92-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="bcc92-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bcc92-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc92-103">Ruft die Anmeldeinformationen für eine Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="bcc92-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcc92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcc92-104">SYNTAX</span></span>

### <span data-ttu-id="bcc92-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bcc92-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcc92-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcc92-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcc92-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcc92-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcc92-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bcc92-108">DESCRIPTION</span></span>
<span data-ttu-id="bcc92-109">Das Get-AzureRmContainerRegistryCredential-Cmdlet ruft die Anmeldeinformationen für eine Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="bcc92-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="bcc92-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bcc92-110">EXAMPLES</span></span>

### <span data-ttu-id="bcc92-111">Beispiel 1: Abrufen der Anmeldeinformationen für eine Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="bcc92-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="bcc92-112">Dieser Befehl ruft die Anmeldeinformationen für die angegebene Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="bcc92-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="bcc92-113">Administrator Benutzer muss für die Container Registrierung \` myregistry aktiviert sein \` , um Anmeldeinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bcc92-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="bcc92-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcc92-114">PARAMETERS</span></span>

### <span data-ttu-id="bcc92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc92-115">-DefaultProfile</span></span>
<span data-ttu-id="bcc92-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bcc92-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcc92-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bcc92-117">-Name</span></span>
<span data-ttu-id="bcc92-118">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="bcc92-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="bcc92-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="bcc92-119">-Registry</span></span>
<span data-ttu-id="bcc92-120">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="bcc92-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc92-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc92-121">-ResourceGroupName</span></span>
<span data-ttu-id="bcc92-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bcc92-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="bcc92-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bcc92-123">-ResourceId</span></span>
<span data-ttu-id="bcc92-124">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="bcc92-124">The container registry resource id</span></span>

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

### <span data-ttu-id="bcc92-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc92-125">CommonParameters</span></span>
<span data-ttu-id="bcc92-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcc92-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc92-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcc92-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc92-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bcc92-128">INPUTS</span></span>

### <span data-ttu-id="bcc92-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bcc92-129">System.String</span></span>

## <span data-ttu-id="bcc92-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bcc92-130">OUTPUTS</span></span>

### <span data-ttu-id="bcc92-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="bcc92-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="bcc92-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="bcc92-132">NOTES</span></span>

## <span data-ttu-id="bcc92-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bcc92-133">RELATED LINKS</span></span>

[<span data-ttu-id="bcc92-134">Neu – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bcc92-134">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="bcc92-135">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bcc92-135">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="bcc92-136">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="bcc92-136">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

