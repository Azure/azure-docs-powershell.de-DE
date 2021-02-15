---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174244"
---
# <span data-ttu-id="6cf74-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="6cf74-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="6cf74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cf74-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf74-103">Erstellen neuer benutzerdefinierter Ressourcen für die iot-Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="6cf74-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="6cf74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cf74-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cf74-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6cf74-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf74-106">Das Cmdlet AzIotSecuritySolutionUserDefinedResourcesObject erstellt ein neues benutzerdefiniertes Ressourcenobjekt für die iot-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="6cf74-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="6cf74-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6cf74-107">EXAMPLES</span></span>

### <span data-ttu-id="6cf74-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6cf74-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="6cf74-109">Erstellen neuer benutzerdefinierter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6cf74-109">Create new user defined resources</span></span>

## <span data-ttu-id="6cf74-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cf74-110">PARAMETERS</span></span>

### <span data-ttu-id="6cf74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf74-111">-DefaultProfile</span></span>
<span data-ttu-id="6cf74-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6cf74-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cf74-113">-Query</span><span class="sxs-lookup"><span data-stu-id="6cf74-113">-Query</span></span>
<span data-ttu-id="6cf74-114">Abfrage.</span><span class="sxs-lookup"><span data-stu-id="6cf74-114">Query.</span></span>

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

### <span data-ttu-id="6cf74-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="6cf74-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="6cf74-116">"Abonnements abfragen".</span><span class="sxs-lookup"><span data-stu-id="6cf74-116">Query subscriptions.</span></span>

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

### <span data-ttu-id="6cf74-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf74-117">CommonParameters</span></span>
<span data-ttu-id="6cf74-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cf74-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf74-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cf74-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf74-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6cf74-120">INPUTS</span></span>

### <span data-ttu-id="6cf74-121">Keine</span><span class="sxs-lookup"><span data-stu-id="6cf74-121">None</span></span>

## <span data-ttu-id="6cf74-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6cf74-122">OUTPUTS</span></span>

### <span data-ttu-id="6cf74-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="6cf74-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="6cf74-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6cf74-124">NOTES</span></span>

## <span data-ttu-id="6cf74-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6cf74-125">RELATED LINKS</span></span>
