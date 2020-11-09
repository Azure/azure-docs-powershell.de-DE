---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302019"
---
# <span data-ttu-id="f398a-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f398a-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="f398a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f398a-102">SYNOPSIS</span></span>
<span data-ttu-id="f398a-103">Ruft eine private Link Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="f398a-103">Gets a private link resource.</span></span>

## <span data-ttu-id="f398a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f398a-104">SYNTAX</span></span>

### <span data-ttu-id="f398a-105">ByPrivateLinkResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="f398a-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f398a-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="f398a-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="f398a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f398a-107">DESCRIPTION</span></span>
<span data-ttu-id="f398a-108">Das Cmdlet " **Get-AzPrivateLinkResource** " ruft alle Verknüpfungs Ressourcen ab, die PrivateLinkResource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f398a-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="f398a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f398a-109">EXAMPLES</span></span>

### <span data-ttu-id="f398a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f398a-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="f398a-111">In diesem Beispiel werden alle privaten Link Ressourcen nbelong SQL Server mit dem Namen MySQL aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f398a-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="f398a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f398a-112">PARAMETERS</span></span>

### <span data-ttu-id="f398a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f398a-113">-DefaultProfile</span></span>
<span data-ttu-id="f398a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f398a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f398a-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f398a-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="f398a-116">Die Azure Resource Manager-ID der privaten Verknüpfungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="f398a-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="f398a-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="f398a-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="f398a-118">Der Ressourcentyp "privater Link".</span><span class="sxs-lookup"><span data-stu-id="f398a-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f398a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f398a-119">-ResourceGroupName</span></span>
<span data-ttu-id="f398a-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f398a-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f398a-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f398a-121">-ServiceName</span></span>
<span data-ttu-id="f398a-122">Der Name des privaten Link Diensts.</span><span class="sxs-lookup"><span data-stu-id="f398a-122">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f398a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f398a-123">CommonParameters</span></span>
<span data-ttu-id="f398a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f398a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f398a-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f398a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f398a-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f398a-126">INPUTS</span></span>

### <span data-ttu-id="f398a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f398a-127">System.String</span></span>

## <span data-ttu-id="f398a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f398a-128">OUTPUTS</span></span>

### <span data-ttu-id="f398a-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f398a-129">System.Boolean</span></span>

## <span data-ttu-id="f398a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f398a-130">NOTES</span></span>

## <span data-ttu-id="f398a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f398a-131">RELATED LINKS</span></span>
