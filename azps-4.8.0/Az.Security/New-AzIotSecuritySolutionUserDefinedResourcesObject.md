---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174187"
---
# <span data-ttu-id="4ae1c-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="4ae1c-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="4ae1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ae1c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae1c-103">Erstellen neuer benutzerdefinierter Ressourcen für viel Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="4ae1c-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="4ae1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ae1c-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ae1c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ae1c-105">DESCRIPTION</span></span>
<span data-ttu-id="4ae1c-106">Das AzIotSecuritySolutionUserDefinedResourcesObject-Cmdlet erstellt ein neues benutzerdefiniertes Ressourcenobjekt für die viel Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="4ae1c-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="4ae1c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ae1c-107">EXAMPLES</span></span>

### <span data-ttu-id="4ae1c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ae1c-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="4ae1c-109">Erstellen neuer benutzerdefinierter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4ae1c-109">Create new user defined resources</span></span>

## <span data-ttu-id="4ae1c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ae1c-110">PARAMETERS</span></span>

### <span data-ttu-id="4ae1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae1c-111">-DefaultProfile</span></span>
<span data-ttu-id="4ae1c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ae1c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ae1c-113">-Query</span><span class="sxs-lookup"><span data-stu-id="4ae1c-113">-Query</span></span>
<span data-ttu-id="4ae1c-114">Abfrage.</span><span class="sxs-lookup"><span data-stu-id="4ae1c-114">Query.</span></span>

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

### <span data-ttu-id="4ae1c-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="4ae1c-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="4ae1c-116">Abfrage Abonnements.</span><span class="sxs-lookup"><span data-stu-id="4ae1c-116">Query subscriptions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae1c-117">CommonParameters</span></span>
<span data-ttu-id="4ae1c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ae1c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae1c-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ae1c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae1c-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ae1c-120">INPUTS</span></span>

### <span data-ttu-id="4ae1c-121">Keine</span><span class="sxs-lookup"><span data-stu-id="4ae1c-121">None</span></span>

## <span data-ttu-id="4ae1c-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ae1c-122">OUTPUTS</span></span>

### <span data-ttu-id="4ae1c-123">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="4ae1c-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="4ae1c-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ae1c-124">NOTES</span></span>

## <span data-ttu-id="4ae1c-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ae1c-125">RELATED LINKS</span></span>
