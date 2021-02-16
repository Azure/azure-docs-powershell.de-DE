---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79b61501a56913fedb2a003d7aea1a041bfab4d5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412281"
---
# <span data-ttu-id="c93bb-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="c93bb-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="c93bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c93bb-102">SYNOPSIS</span></span>
<span data-ttu-id="c93bb-103">Ruft einen Websitewiederherstellungsserver ab, der einen Websitewiederherstellungstresor registriert hat.</span><span class="sxs-lookup"><span data-stu-id="c93bb-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="c93bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c93bb-104">SYNTAX</span></span>

### <span data-ttu-id="c93bb-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="c93bb-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c93bb-106">ById</span><span class="sxs-lookup"><span data-stu-id="c93bb-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c93bb-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c93bb-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c93bb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c93bb-108">DESCRIPTION</span></span>
<span data-ttu-id="c93bb-109">Das **Cmdlet "Get-AzureSiteRecoveryServer"** ruft Informationen zu azure-Websitewiederherstellungsservern ab, die im aktuellen Websitewiederherstellungstresor registriert sind.</span><span class="sxs-lookup"><span data-stu-id="c93bb-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="c93bb-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c93bb-110">EXAMPLES</span></span>

### <span data-ttu-id="c93bb-111">Beispiel 1: Informationen zu einem Websitewiederherstellungsserver</span><span class="sxs-lookup"><span data-stu-id="c93bb-111">Example 1: Get information about a Site Recovery server</span></span>
```
PS C:\> Get-AzureSiteRecoveryServer
ID              : cd7dec80-1144-4531-9ab3-888b8ab39bee
Name            : server1.contoso.com
LastHeartbeat   : 9/23/2014 3:51:22 PM
ProviderVersion : 3.5.520.0
ServerVersion   : 3.2.7634.0

ID              : f5e713fe-5b6d-4641-9690-6fe74c976b8e
Name            : Server2.contoso.com
LastHeartbeat   : 8/13/2014 2:28:58 PM
ProviderVersion : 3.5
ServerVersion   : 3.2.7510.0
```

<span data-ttu-id="c93bb-112">Dieser Befehl ruft Informationen zu einem Azure Site Recovery Server ab.</span><span class="sxs-lookup"><span data-stu-id="c93bb-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="c93bb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c93bb-113">PARAMETERS</span></span>

### <span data-ttu-id="c93bb-114">-ID</span><span class="sxs-lookup"><span data-stu-id="c93bb-114">-Id</span></span>
<span data-ttu-id="c93bb-115">Gibt die ID eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="c93bb-115">Specifies the ID of a server.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93bb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c93bb-116">-Name</span></span>
<span data-ttu-id="c93bb-117">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="c93bb-117">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93bb-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="c93bb-118">-Profile</span></span>
<span data-ttu-id="c93bb-119">Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c93bb-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c93bb-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c93bb-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93bb-121">CommonParameters</span></span>
<span data-ttu-id="c93bb-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c93bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93bb-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c93bb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93bb-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c93bb-124">INPUTS</span></span>

## <span data-ttu-id="c93bb-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c93bb-125">OUTPUTS</span></span>

## <span data-ttu-id="c93bb-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c93bb-126">NOTES</span></span>

## <span data-ttu-id="c93bb-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c93bb-127">RELATED LINKS</span></span>




