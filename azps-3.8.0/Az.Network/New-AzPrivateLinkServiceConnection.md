---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
ms.openlocfilehash: 74f531e48ca873d3853aba3312d6bb10edccdfaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003467"
---
# <span data-ttu-id="ed47b-101">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ed47b-101">New-AzPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="ed47b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed47b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed47b-103">Erstellt eine Verbindungskonfiguration für private Verbindungsdienste.</span><span class="sxs-lookup"><span data-stu-id="ed47b-103">Creates a private link service connection configuration.</span></span>

## <span data-ttu-id="ed47b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed47b-104">SYNTAX</span></span>

### <span data-ttu-id="ed47b-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed47b-105">SetByResource (Default)</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkService <PSPrivateLinkService>
 [-GroupId <String[]>] [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed47b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed47b-106">SetByResourceId</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkServiceId <String> [-GroupId <String[]>]
 [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed47b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed47b-107">DESCRIPTION</span></span>
<span data-ttu-id="ed47b-108">**Das Cmdlet New-AzPrivateLinkServiceConnection** erstellt eine Verbindungskonfiguration für den privaten Verbindungsdienst.</span><span class="sxs-lookup"><span data-stu-id="ed47b-108">**The New-AzPrivateLinkServiceConnection** cmdlet creates a private link service connection configuration.</span></span>

## <span data-ttu-id="ed47b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed47b-109">EXAMPLES</span></span>

### <span data-ttu-id="ed47b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed47b-110">Example 1</span></span>
```
New-AzPrivateLinkServiceConnection -Name MyPLSConnection -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
```

<span data-ttu-id="ed47b-111">In diesem Beispiel wird ein Verbindungsobjekt für einen privaten Verbindungsdienst im Arbeitsspeicher erstellt, das beim Erstellen eines privaten Endpunkts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed47b-111">This example create a private link service connection object in memory for using in creating private endpoint.</span></span>

## <span data-ttu-id="ed47b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed47b-112">PARAMETERS</span></span>

### <span data-ttu-id="ed47b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed47b-113">-DefaultProfile</span></span>
<span data-ttu-id="ed47b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed47b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed47b-115">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="ed47b-115">-GroupId</span></span>
<span data-ttu-id="ed47b-116">Die Liste der Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="ed47b-116">The list of group id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed47b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ed47b-117">-Name</span></span>
<span data-ttu-id="ed47b-118">Der Name des Diensts für private Links.</span><span class="sxs-lookup"><span data-stu-id="ed47b-118">The name of private link service.</span></span>

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

### <span data-ttu-id="ed47b-119">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ed47b-119">-PrivateLinkService</span></span>
<span data-ttu-id="ed47b-120">Der private Link-Dienst.</span><span class="sxs-lookup"><span data-stu-id="ed47b-120">The private link service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed47b-121">-PrivateLinkServiceId</span><span class="sxs-lookup"><span data-stu-id="ed47b-121">-PrivateLinkServiceId</span></span>
<span data-ttu-id="ed47b-122">Die ID des Diensts für private Links.</span><span class="sxs-lookup"><span data-stu-id="ed47b-122">The id of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed47b-123">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="ed47b-123">-RequestMessage</span></span>
<span data-ttu-id="ed47b-124">Die Anforderungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="ed47b-124">The request message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed47b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed47b-125">CommonParameters</span></span>
<span data-ttu-id="ed47b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed47b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed47b-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed47b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed47b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed47b-128">INPUTS</span></span>

### <span data-ttu-id="ed47b-129">Keine</span><span class="sxs-lookup"><span data-stu-id="ed47b-129">None</span></span>

## <span data-ttu-id="ed47b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed47b-130">OUTPUTS</span></span>

### <span data-ttu-id="ed47b-131">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ed47b-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="ed47b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed47b-132">NOTES</span></span>

## <span data-ttu-id="ed47b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed47b-133">RELATED LINKS</span></span>

[<span data-ttu-id="ed47b-134">Neu – AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed47b-134">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)