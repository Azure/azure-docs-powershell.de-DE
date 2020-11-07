---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 3b9b31530d467f0c31ea3ade4968118042fee47b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820468"
---
# <span data-ttu-id="d2409-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="d2409-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="d2409-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2409-102">SYNOPSIS</span></span>
<span data-ttu-id="d2409-103">Ruft die Anmeldeinformationen für eine Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="d2409-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="d2409-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2409-104">SYNTAX</span></span>

### <span data-ttu-id="d2409-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2409-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2409-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2409-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2409-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2409-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2409-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2409-108">DESCRIPTION</span></span>
<span data-ttu-id="d2409-109">Das Get-AzContainerRegistryCredential-Cmdlet ruft die Anmeldeinformationen für eine Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="d2409-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="d2409-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2409-110">EXAMPLES</span></span>

### <span data-ttu-id="d2409-111">Beispiel 1: Abrufen der Anmeldeinformationen für eine Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="d2409-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="d2409-112">Dieser Befehl ruft die Anmeldeinformationen für die angegebene Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="d2409-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="d2409-113">Administrator Benutzer muss für die Container Registrierung \` myregistry aktiviert sein \` , um Anmeldeinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d2409-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="d2409-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2409-114">PARAMETERS</span></span>

### <span data-ttu-id="d2409-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2409-115">-DefaultProfile</span></span>
<span data-ttu-id="d2409-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d2409-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2409-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d2409-117">-Name</span></span>
<span data-ttu-id="d2409-118">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="d2409-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="d2409-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="d2409-119">-Registry</span></span>
<span data-ttu-id="d2409-120">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d2409-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="d2409-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2409-121">-ResourceGroupName</span></span>
<span data-ttu-id="d2409-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d2409-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="d2409-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d2409-123">-ResourceId</span></span>
<span data-ttu-id="d2409-124">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="d2409-124">The container registry resource id</span></span>

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

### <span data-ttu-id="d2409-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2409-125">CommonParameters</span></span>
<span data-ttu-id="d2409-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2409-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2409-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2409-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2409-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2409-128">INPUTS</span></span>

### <span data-ttu-id="d2409-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d2409-129">System.String</span></span>

## <span data-ttu-id="d2409-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2409-130">OUTPUTS</span></span>

### <span data-ttu-id="d2409-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="d2409-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="d2409-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2409-132">NOTES</span></span>

## <span data-ttu-id="d2409-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2409-133">RELATED LINKS</span></span>

[<span data-ttu-id="d2409-134">Neu – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d2409-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="d2409-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d2409-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="d2409-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="d2409-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

