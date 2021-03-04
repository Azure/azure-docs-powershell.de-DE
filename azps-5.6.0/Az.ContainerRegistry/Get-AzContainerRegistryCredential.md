---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 5e20ae556cba16263d8b650de869b174236ccbd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945245"
---
# <span data-ttu-id="1be77-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="1be77-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="1be77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1be77-102">SYNOPSIS</span></span>
<span data-ttu-id="1be77-103">Ruft die Anmeldeinformationen für eine Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="1be77-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="1be77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1be77-104">SYNTAX</span></span>

### <span data-ttu-id="1be77-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1be77-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1be77-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1be77-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1be77-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1be77-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1be77-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1be77-108">DESCRIPTION</span></span>
<span data-ttu-id="1be77-109">Das Get-AzContainerRegistryCredential-Cmdlet ruft die Anmeldeinformationen für eine Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="1be77-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="1be77-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1be77-110">EXAMPLES</span></span>

### <span data-ttu-id="1be77-111">Beispiel 1: Erhalten der Anmeldeinformationen für eine Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="1be77-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="1be77-112">Dieser Befehl ruft die Anmeldeinformationen für die angegebene Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="1be77-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="1be77-113">Administratorbenutzer müssen für die Containerregistrierung \` MyRegistry aktiviert sein, \` um Anmeldeinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1be77-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="1be77-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1be77-114">PARAMETERS</span></span>

### <span data-ttu-id="1be77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be77-115">-DefaultProfile</span></span>
<span data-ttu-id="1be77-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1be77-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1be77-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1be77-117">-Name</span></span>
<span data-ttu-id="1be77-118">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="1be77-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="1be77-119">-Registrierung</span><span class="sxs-lookup"><span data-stu-id="1be77-119">-Registry</span></span>
<span data-ttu-id="1be77-120">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="1be77-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="1be77-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1be77-121">-ResourceGroupName</span></span>
<span data-ttu-id="1be77-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="1be77-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="1be77-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1be77-123">-ResourceId</span></span>
<span data-ttu-id="1be77-124">Die Containerregistrierungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="1be77-124">The container registry resource id</span></span>

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

### <span data-ttu-id="1be77-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be77-125">CommonParameters</span></span>
<span data-ttu-id="1be77-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1be77-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be77-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1be77-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be77-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1be77-128">INPUTS</span></span>

### <span data-ttu-id="1be77-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1be77-129">System.String</span></span>

## <span data-ttu-id="1be77-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1be77-130">OUTPUTS</span></span>

### <span data-ttu-id="1be77-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="1be77-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="1be77-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1be77-132">NOTES</span></span>

## <span data-ttu-id="1be77-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1be77-133">RELATED LINKS</span></span>

[<span data-ttu-id="1be77-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1be77-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="1be77-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1be77-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="1be77-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="1be77-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

