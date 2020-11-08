---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175796"
---
# <span data-ttu-id="51191-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="51191-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="51191-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51191-102">SYNOPSIS</span></span>
<span data-ttu-id="51191-103">Melden Sie sich bei einer Azure Container-Registrierung an.</span><span class="sxs-lookup"><span data-stu-id="51191-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="51191-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51191-104">SYNTAX</span></span>

### <span data-ttu-id="51191-105">WithoutNameAndPasswordParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="51191-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51191-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="51191-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51191-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51191-107">DESCRIPTION</span></span>
<span data-ttu-id="51191-108">Melden Sie sich bei einer Azure Container-Registrierung an.</span><span class="sxs-lookup"><span data-stu-id="51191-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="51191-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51191-109">EXAMPLES</span></span>

### <span data-ttu-id="51191-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="51191-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="51191-111">Melden Sie sich bei ACR ohne Anmeldeinformationen an, wenn Sie sich bereits beim Azure-Konto anmelden.</span><span class="sxs-lookup"><span data-stu-id="51191-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="51191-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="51191-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="51191-113">Melden Sie sich bei ACR mit Administrator-Nutzernamen/Kennwort an, wenn Administrator-Benutzer aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="51191-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="51191-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="51191-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="51191-115">Melden Sie sich bei ACR mit der Dienstprinzipal-Anwendungs-ID und dem Kennwort an.</span><span class="sxs-lookup"><span data-stu-id="51191-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="51191-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="51191-116">PARAMETERS</span></span>

### <span data-ttu-id="51191-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51191-117">-DefaultProfile</span></span>
<span data-ttu-id="51191-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51191-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51191-119">-Name</span><span class="sxs-lookup"><span data-stu-id="51191-119">-Name</span></span>
<span data-ttu-id="51191-120">Azure Container-Registrierungs Name.</span><span class="sxs-lookup"><span data-stu-id="51191-120">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="51191-121">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="51191-121">-Password</span></span>
<span data-ttu-id="51191-122">Kennwort für die Azure-Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="51191-122">Password For Azure Container Registry.</span></span>

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

### <span data-ttu-id="51191-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="51191-123">-UserName</span></span>
<span data-ttu-id="51191-124">Benutzer Name für die Azure-Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="51191-124">User Name For Azure Container Registry.</span></span>

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

### <span data-ttu-id="51191-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51191-125">CommonParameters</span></span>
<span data-ttu-id="51191-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51191-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51191-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51191-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51191-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51191-128">INPUTS</span></span>

### <span data-ttu-id="51191-129">System. String</span><span class="sxs-lookup"><span data-stu-id="51191-129">System.String</span></span>

## <span data-ttu-id="51191-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51191-130">OUTPUTS</span></span>

### <span data-ttu-id="51191-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51191-131">System.Boolean</span></span>

## <span data-ttu-id="51191-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="51191-132">NOTES</span></span>

## <span data-ttu-id="51191-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51191-133">RELATED LINKS</span></span>
