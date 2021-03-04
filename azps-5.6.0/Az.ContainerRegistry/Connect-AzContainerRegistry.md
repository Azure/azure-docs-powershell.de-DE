---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: be045303db770cbba919d27ed9563aa64283572c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945257"
---
# <span data-ttu-id="2a299-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2a299-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="2a299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a299-102">SYNOPSIS</span></span>
<span data-ttu-id="2a299-103">Melden Sie sich bei einer Azure-Containerregistrierung an.</span><span class="sxs-lookup"><span data-stu-id="2a299-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="2a299-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a299-104">SYNTAX</span></span>

### <span data-ttu-id="2a299-105">WithoutNameAndPasswordParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a299-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a299-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a299-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a299-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a299-107">DESCRIPTION</span></span>
<span data-ttu-id="2a299-108">Melden Sie sich bei einer Azure-Containerregistrierung an.</span><span class="sxs-lookup"><span data-stu-id="2a299-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="2a299-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a299-109">EXAMPLES</span></span>

### <span data-ttu-id="2a299-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2a299-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="2a299-111">Melden Sie sich bei ACR ohne Anmeldeinformationen an, wenn Sie sich bereits bei einem Azure-Konto anmelden.</span><span class="sxs-lookup"><span data-stu-id="2a299-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="2a299-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2a299-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="2a299-113">Melden Sie sich bei ACR mit Administratorbenutzername/Kennwort an, wenn der Administratorbenutzer aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="2a299-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="2a299-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2a299-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="2a299-115">Melden Sie sich bei ACR mit Dienstprinzipalanwendungs-ID und Kennwort an.</span><span class="sxs-lookup"><span data-stu-id="2a299-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="2a299-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2a299-116">PARAMETERS</span></span>

### <span data-ttu-id="2a299-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a299-117">-DefaultProfile</span></span>
<span data-ttu-id="2a299-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a299-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a299-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2a299-119">-Name</span></span>
<span data-ttu-id="2a299-120">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="2a299-120">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="2a299-121">-Password</span><span class="sxs-lookup"><span data-stu-id="2a299-121">-Password</span></span>
<span data-ttu-id="2a299-122">Kennwort für azure container registry.</span><span class="sxs-lookup"><span data-stu-id="2a299-122">Password For Azure Container Registry.</span></span>

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

### <span data-ttu-id="2a299-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="2a299-123">-UserName</span></span>
<span data-ttu-id="2a299-124">Benutzername für Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="2a299-124">User Name For Azure Container Registry.</span></span>

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

### <span data-ttu-id="2a299-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a299-125">CommonParameters</span></span>
<span data-ttu-id="2a299-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a299-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a299-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a299-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a299-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a299-128">INPUTS</span></span>

### <span data-ttu-id="2a299-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2a299-129">System.String</span></span>

## <span data-ttu-id="2a299-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a299-130">OUTPUTS</span></span>

### <span data-ttu-id="2a299-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a299-131">System.Boolean</span></span>

## <span data-ttu-id="2a299-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2a299-132">NOTES</span></span>

## <span data-ttu-id="2a299-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2a299-133">RELATED LINKS</span></span>
