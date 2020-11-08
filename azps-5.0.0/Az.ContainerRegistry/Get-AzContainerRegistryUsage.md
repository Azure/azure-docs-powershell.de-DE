---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 691d8cf006e720d706d2473f76ff8660927e73ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175788"
---
# <span data-ttu-id="ad128-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ad128-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="ad128-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad128-102">SYNOPSIS</span></span>
<span data-ttu-id="ad128-103">Abrufen der Verwendung einer Azure Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="ad128-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ad128-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad128-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad128-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad128-105">DESCRIPTION</span></span>
<span data-ttu-id="ad128-106">Abrufen der Verwendung einer Azure Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="ad128-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ad128-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad128-107">EXAMPLES</span></span>

### <span data-ttu-id="ad128-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad128-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="ad128-109">Abrufen der Verwendung einer Azure Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="ad128-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ad128-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad128-110">PARAMETERS</span></span>

### <span data-ttu-id="ad128-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad128-111">-DefaultProfile</span></span>
<span data-ttu-id="ad128-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad128-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad128-113">-Registryname</span><span class="sxs-lookup"><span data-stu-id="ad128-113">-RegistryName</span></span>
<span data-ttu-id="ad128-114">Ziel Registrierungsname</span><span class="sxs-lookup"><span data-stu-id="ad128-114">Target registry name.</span></span>

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

### <span data-ttu-id="ad128-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad128-115">-ResourceGroupName</span></span>
<span data-ttu-id="ad128-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ad128-116">Resource group name.</span></span>

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

### <span data-ttu-id="ad128-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad128-117">CommonParameters</span></span>
<span data-ttu-id="ad128-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad128-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad128-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad128-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad128-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad128-120">INPUTS</span></span>

### <span data-ttu-id="ad128-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ad128-121">System.String</span></span>

## <span data-ttu-id="ad128-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad128-122">OUTPUTS</span></span>

### <span data-ttu-id="ad128-123">Microsoft. Azure. Commands. ContainerRegistry. Models. PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ad128-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="ad128-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad128-124">NOTES</span></span>

## <span data-ttu-id="ad128-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad128-125">RELATED LINKS</span></span>
