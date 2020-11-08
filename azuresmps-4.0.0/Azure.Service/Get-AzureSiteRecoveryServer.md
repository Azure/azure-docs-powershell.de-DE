---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4081d6d072aadd6a4ae7d09ff57748a8f2cb697
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005786"
---
# <span data-ttu-id="857a8-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="857a8-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="857a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="857a8-102">SYNOPSIS</span></span>
<span data-ttu-id="857a8-103">Ruft Website Wiederherstellungsserver ab, die einen Standort Wiederherstellungs Tresor registriert haben.</span><span class="sxs-lookup"><span data-stu-id="857a8-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="857a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="857a8-104">SYNTAX</span></span>

### <span data-ttu-id="857a8-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="857a8-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="857a8-106">ById</span><span class="sxs-lookup"><span data-stu-id="857a8-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="857a8-107">ByName</span><span class="sxs-lookup"><span data-stu-id="857a8-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="857a8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="857a8-108">DESCRIPTION</span></span>
<span data-ttu-id="857a8-109">Das Cmdlet " **Get-AzureSiteRecoveryServer** " Ruft Informationen zu Azure Site Recovery-Servern ab, die für das aktuelle Standort Wiederherstellungs Depot registriert sind.</span><span class="sxs-lookup"><span data-stu-id="857a8-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="857a8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="857a8-110">EXAMPLES</span></span>

### <span data-ttu-id="857a8-111">Beispiel 1: Abrufen von Informationen zu einem Website Wiederherstellungsserver</span><span class="sxs-lookup"><span data-stu-id="857a8-111">Example 1: Get information about a Site Recovery server</span></span>
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

<span data-ttu-id="857a8-112">Dieser Befehl ruft Informationen zu einem Azure Site Recovery Server ab.</span><span class="sxs-lookup"><span data-stu-id="857a8-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="857a8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="857a8-113">PARAMETERS</span></span>

### <span data-ttu-id="857a8-114">-ID</span><span class="sxs-lookup"><span data-stu-id="857a8-114">-Id</span></span>
<span data-ttu-id="857a8-115">Gibt die ID eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="857a8-115">Specifies the ID of a server.</span></span>

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

### <span data-ttu-id="857a8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="857a8-116">-Name</span></span>
<span data-ttu-id="857a8-117">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="857a8-117">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="857a8-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="857a8-118">-Profile</span></span>
<span data-ttu-id="857a8-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="857a8-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="857a8-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="857a8-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="857a8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857a8-121">CommonParameters</span></span>
<span data-ttu-id="857a8-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="857a8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857a8-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="857a8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857a8-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="857a8-124">INPUTS</span></span>

## <span data-ttu-id="857a8-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="857a8-125">OUTPUTS</span></span>

## <span data-ttu-id="857a8-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="857a8-126">NOTES</span></span>

## <span data-ttu-id="857a8-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="857a8-127">RELATED LINKS</span></span>

[<span data-ttu-id="857a8-128">Azure Site Recovery Services-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="857a8-128">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


