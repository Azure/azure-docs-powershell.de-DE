---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 78DE0AD2-6210-4604-89A8-41915D58BD68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c40cb0fd38953ff46fa1138dc91f0b9e97ece75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005782"
---
# <span data-ttu-id="e5331-101">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="e5331-101">Get-AzureSiteRecoveryStorage</span></span>

## <span data-ttu-id="e5331-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5331-102">SYNOPSIS</span></span>
<span data-ttu-id="e5331-103">Ruft Speicher für die Websitewiederherstellung für einen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="e5331-103">Gets Site Recovery Storages for a vault.</span></span>

## <span data-ttu-id="e5331-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5331-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorage -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e5331-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5331-105">DESCRIPTION</span></span>
<span data-ttu-id="e5331-106">Das Cmdlet " **Get-AzureSiteRecoveryStorage** " ruft Azure Site Recovery-Speicher für das aktuelle Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="e5331-106">The **Get-AzureSiteRecoveryStorage** cmdlet gets Azure Site Recovery Storages for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e5331-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5331-107">EXAMPLES</span></span>

### <span data-ttu-id="e5331-108">Beispiel 1: Abrufen von Speicherplatz für die Standortwiederherstellung</span><span class="sxs-lookup"><span data-stu-id="e5331-108">Example 1: Get site recovery storage</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorage -Server $Servers[0]
Name           : phase2PrimaryStorageClassification
ID             : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
FabricObjectID : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM

Name           : phase2RecoveryStorageClassification
ID             : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
FabricObjectID : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM
```

<span data-ttu-id="e5331-109">Das Cmdlet "erster Befehl" Ruft Server für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryServer** ab.</span><span class="sxs-lookup"><span data-stu-id="e5331-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="e5331-110">Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="e5331-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="e5331-111">Mit dem zweiten Befehl wird der Standort Wiederherstellungs Speicher für den ersten Server im $Servers-Array abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e5331-111">The second command gets the site recovery storage for the first server in the $Servers array.</span></span>

## <span data-ttu-id="e5331-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5331-112">PARAMETERS</span></span>

### <span data-ttu-id="e5331-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="e5331-113">-Profile</span></span>
<span data-ttu-id="e5331-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e5331-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5331-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e5331-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5331-116">-Server</span><span class="sxs-lookup"><span data-stu-id="e5331-116">-Server</span></span>
<span data-ttu-id="e5331-117">Gibt einen Server für Azure Site Recovery Storage an.</span><span class="sxs-lookup"><span data-stu-id="e5331-117">Specifies a server for Azure Site Recovery Storage.</span></span>
<span data-ttu-id="e5331-118">Verwenden Sie das Cmdlet **Get-AzureSiteRecoveryServer** , um ein **ASRServer** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e5331-118">To obtain an **ASRServer** object, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5331-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5331-119">CommonParameters</span></span>
<span data-ttu-id="e5331-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5331-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5331-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5331-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5331-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5331-122">INPUTS</span></span>

## <span data-ttu-id="e5331-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5331-123">OUTPUTS</span></span>

## <span data-ttu-id="e5331-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5331-124">NOTES</span></span>

## <span data-ttu-id="e5331-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5331-125">RELATED LINKS</span></span>

[<span data-ttu-id="e5331-126">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="e5331-126">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


