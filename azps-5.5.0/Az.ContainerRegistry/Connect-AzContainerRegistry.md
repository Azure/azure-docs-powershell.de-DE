---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 3c702d0572bb8e5bdf41deff599b9da6c5cc2dcf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175828"
---
# <span data-ttu-id="4eab0-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4eab0-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="4eab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eab0-102">SYNOPSIS</span></span>
<span data-ttu-id="4eab0-103">Melden Sie sich bei einer Azure-Containerregistrierung an.</span><span class="sxs-lookup"><span data-stu-id="4eab0-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="4eab0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4eab0-104">SYNTAX</span></span>

### <span data-ttu-id="4eab0-105">WithoutNameAndPasswordParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="4eab0-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eab0-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eab0-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eab0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4eab0-107">DESCRIPTION</span></span>
<span data-ttu-id="4eab0-108">Melden Sie sich bei einer Azure-Containerregistrierung an.</span><span class="sxs-lookup"><span data-stu-id="4eab0-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="4eab0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4eab0-109">EXAMPLES</span></span>

### <span data-ttu-id="4eab0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4eab0-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="4eab0-111">Melden Sie sich bei ACR ohne Anmeldeinformationen an, wenn Sie sich bereits bei einem Azure-Konto anmelden.</span><span class="sxs-lookup"><span data-stu-id="4eab0-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="4eab0-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4eab0-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="4eab0-113">Melden Sie sich bei ACR mit Administratorbenutzernamen/Kennwort an, wenn der Administratorbenutzer aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="4eab0-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="4eab0-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4eab0-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="4eab0-115">Melden Sie sich bei ACR mit Dienstprinzipalanwendungs-ID und Kennwort an.</span><span class="sxs-lookup"><span data-stu-id="4eab0-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="4eab0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eab0-116">PARAMETERS</span></span>

### <span data-ttu-id="4eab0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eab0-117">-DefaultProfile</span></span>
<span data-ttu-id="4eab0-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4eab0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eab0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4eab0-119">-Name</span></span>
<span data-ttu-id="4eab0-120">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="4eab0-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eab0-121">-Password</span><span class="sxs-lookup"><span data-stu-id="4eab0-121">-Password</span></span>
<span data-ttu-id="4eab0-122">Kennwort für die Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="4eab0-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eab0-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="4eab0-123">-UserName</span></span>
<span data-ttu-id="4eab0-124">Benutzername für die Azure-Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="4eab0-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eab0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eab0-125">CommonParameters</span></span>
<span data-ttu-id="4eab0-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eab0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eab0-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4eab0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eab0-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4eab0-128">INPUTS</span></span>

### <span data-ttu-id="4eab0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4eab0-129">System.String</span></span>

## <span data-ttu-id="4eab0-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4eab0-130">OUTPUTS</span></span>

### <span data-ttu-id="4eab0-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4eab0-131">System.Boolean</span></span>

## <span data-ttu-id="4eab0-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4eab0-132">NOTES</span></span>

## <span data-ttu-id="4eab0-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4eab0-133">RELATED LINKS</span></span>
