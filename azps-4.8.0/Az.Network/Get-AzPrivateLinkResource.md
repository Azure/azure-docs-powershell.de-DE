---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 3ba277ccee3a07f71677628fdc0a985225cdf724
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165255"
---
# <span data-ttu-id="54594-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="54594-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="54594-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54594-102">SYNOPSIS</span></span>
<span data-ttu-id="54594-103">Ruft eine private Link Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="54594-103">Gets a private link resource.</span></span>

## <span data-ttu-id="54594-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54594-104">SYNTAX</span></span>

### <span data-ttu-id="54594-105">ByPrivateLinkResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="54594-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54594-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54594-106">DESCRIPTION</span></span>
<span data-ttu-id="54594-107">Das Cmdlet " **Get-AzPrivateLinkResource** " ruft alle Verknüpfungs Ressourcen ab, die PrivateLinkResource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="54594-107">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="54594-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54594-108">EXAMPLES</span></span>

### <span data-ttu-id="54594-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54594-109">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="54594-110">In diesem Beispiel werden alle privaten Link Ressourcen nbelong SQL Server mit dem Namen MySQL aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="54594-110">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="54594-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="54594-111">PARAMETERS</span></span>

### <span data-ttu-id="54594-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54594-112">-DefaultProfile</span></span>
<span data-ttu-id="54594-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54594-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54594-114">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="54594-114">-PrivateLinkResourceId</span></span>
<span data-ttu-id="54594-115">Die Azure Resource Manager-ID der privaten Verknüpfungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="54594-115">The Azure resource manager id of the private link resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54594-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54594-116">CommonParameters</span></span>
<span data-ttu-id="54594-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54594-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54594-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54594-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54594-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54594-119">INPUTS</span></span>

### <span data-ttu-id="54594-120">System. String</span><span class="sxs-lookup"><span data-stu-id="54594-120">System.String</span></span>

## <span data-ttu-id="54594-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54594-121">OUTPUTS</span></span>

### <span data-ttu-id="54594-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54594-122">System.Boolean</span></span>

## <span data-ttu-id="54594-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="54594-123">NOTES</span></span>

## <span data-ttu-id="54594-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54594-124">RELATED LINKS</span></span>
