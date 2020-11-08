---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006821"
---
# <span data-ttu-id="a0b50-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="a0b50-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="a0b50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0b50-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b50-103">Verschaffen Sie sich einen Überblick über den Zustand des Netzwerkressourcen Anbieters.</span><span class="sxs-lookup"><span data-stu-id="a0b50-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="a0b50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0b50-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="a0b50-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0b50-105">DESCRIPTION</span></span>
<span data-ttu-id="a0b50-106">Verschaffen Sie sich einen Überblick über den Zustand des Netzwerkressourcen Anbieters.</span><span class="sxs-lookup"><span data-stu-id="a0b50-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="a0b50-107">Einzelne Eigenschaften bieten detaillierte Zählungen der Ressourcennutzung und des Status nach Komponenten.</span><span class="sxs-lookup"><span data-stu-id="a0b50-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="a0b50-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0b50-108">EXAMPLES</span></span>

### <span data-ttu-id="a0b50-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0b50-109">EXAMPLE 1</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="a0b50-110">Netzwerkadministrator-Übersicht abrufen.</span><span class="sxs-lookup"><span data-stu-id="a0b50-110">Get network admin overview.</span></span>

### <span data-ttu-id="a0b50-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a0b50-111">EXAMPLE 2</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="a0b50-112">Abrufen der Nutzung öffentlicher IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="a0b50-112">Get public ip address usage.</span></span>

## <span data-ttu-id="a0b50-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0b50-113">PARAMETERS</span></span>

### <span data-ttu-id="a0b50-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b50-114">CommonParameters</span></span>
<span data-ttu-id="a0b50-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0b50-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b50-116">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0b50-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b50-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0b50-117">INPUTS</span></span>

## <span data-ttu-id="a0b50-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0b50-118">OUTPUTS</span></span>

### <span data-ttu-id="a0b50-119">Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="a0b50-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="a0b50-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0b50-120">NOTES</span></span>

## <span data-ttu-id="a0b50-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0b50-121">RELATED LINKS</span></span>
