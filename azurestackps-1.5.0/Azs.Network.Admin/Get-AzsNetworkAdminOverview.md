---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474998"
---
# <span data-ttu-id="7400c-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="7400c-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="7400c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7400c-102">SYNOPSIS</span></span>
<span data-ttu-id="7400c-103">Verschaffen Sie sich einen Überblick über den Zustand des Netzwerkressourcen Anbieters.</span><span class="sxs-lookup"><span data-stu-id="7400c-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="7400c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7400c-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="7400c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7400c-105">DESCRIPTION</span></span>
<span data-ttu-id="7400c-106">Verschaffen Sie sich einen Überblick über den Zustand des Netzwerkressourcen Anbieters.</span><span class="sxs-lookup"><span data-stu-id="7400c-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="7400c-107">Einzelne Eigenschaften bieten detaillierte Zählungen der Ressourcennutzung und des Status nach Komponenten.</span><span class="sxs-lookup"><span data-stu-id="7400c-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="7400c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7400c-108">EXAMPLES</span></span>

### <span data-ttu-id="7400c-109">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7400c-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="7400c-110">Netzwerkadministrator-Übersicht abrufen.</span><span class="sxs-lookup"><span data-stu-id="7400c-110">Get network admin overview.</span></span>

### <span data-ttu-id="7400c-111">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7400c-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="7400c-112">Abrufen der Nutzung öffentlicher IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="7400c-112">Get public ip address usage.</span></span>

## <span data-ttu-id="7400c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7400c-113">PARAMETERS</span></span>

### <span data-ttu-id="7400c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7400c-114">CommonParameters</span></span>
<span data-ttu-id="7400c-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7400c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7400c-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7400c-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7400c-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7400c-117">INPUTS</span></span>

## <span data-ttu-id="7400c-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7400c-118">OUTPUTS</span></span>

### <span data-ttu-id="7400c-119">Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="7400c-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="7400c-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="7400c-120">NOTES</span></span>

## <span data-ttu-id="7400c-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7400c-121">RELATED LINKS</span></span>

