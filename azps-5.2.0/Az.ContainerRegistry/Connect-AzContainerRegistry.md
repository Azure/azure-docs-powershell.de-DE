---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300907"
---
# <span data-ttu-id="5f6b2-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5f6b2-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="5f6b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f6b2-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6b2-103">Melden Sie sich bei einer Azure-Containerregistrierung an.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="5f6b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f6b2-104">SYNTAX</span></span>

### <span data-ttu-id="5f6b2-105">WithoutNameAndPasswordParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f6b2-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f6b2-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f6b2-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f6b2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f6b2-107">DESCRIPTION</span></span>
<span data-ttu-id="5f6b2-108">Melden Sie sich bei einer Azure-Containerregistrierung an.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="5f6b2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5f6b2-109">EXAMPLES</span></span>

### <span data-ttu-id="5f6b2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f6b2-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="5f6b2-111">Melden Sie sich bei ACR ohne Anmeldeinformationen an, wenn Sie sich bereits bei einem Azure-Konto anmelden.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="5f6b2-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5f6b2-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="5f6b2-113">Melden Sie sich bei ACR mit Administratorbenutzernamen/Kennwort an, wenn der Administratorbenutzer aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="5f6b2-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5f6b2-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="5f6b2-115">Melden Sie sich bei ACR mit Dienstprinzipalanwendungs-ID und Kennwort an.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="5f6b2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f6b2-116">PARAMETERS</span></span>

### <span data-ttu-id="5f6b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6b2-117">-DefaultProfile</span></span>
<span data-ttu-id="5f6b2-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f6b2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5f6b2-119">-Name</span></span>
<span data-ttu-id="5f6b2-120">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f6b2-121">-Password</span><span class="sxs-lookup"><span data-stu-id="5f6b2-121">-Password</span></span>
<span data-ttu-id="5f6b2-122">Kennwort für die Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-122">Password For Azure Container Registry.</span></span>

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

### <span data-ttu-id="5f6b2-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="5f6b2-123">-UserName</span></span>
<span data-ttu-id="5f6b2-124">Benutzername für die Azure-Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-124">User Name For Azure Container Registry.</span></span>

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

### <span data-ttu-id="5f6b2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6b2-125">CommonParameters</span></span>
<span data-ttu-id="5f6b2-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6b2-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f6b2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6b2-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5f6b2-128">INPUTS</span></span>

### <span data-ttu-id="5f6b2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5f6b2-129">System.String</span></span>

## <span data-ttu-id="5f6b2-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5f6b2-130">OUTPUTS</span></span>

### <span data-ttu-id="5f6b2-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5f6b2-131">System.Boolean</span></span>

## <span data-ttu-id="5f6b2-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5f6b2-132">NOTES</span></span>

## <span data-ttu-id="5f6b2-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5f6b2-133">RELATED LINKS</span></span>
