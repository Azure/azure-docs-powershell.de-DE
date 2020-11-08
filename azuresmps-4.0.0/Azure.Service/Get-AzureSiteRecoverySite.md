---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6DD09F28-BFAE-4F9B-BF9C-F09767F9BFEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9151cb5a64b5873ab1c63420a97eb2e7bcffc0ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005783"
---
# <span data-ttu-id="dd5d5-101">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="dd5d5-101">Get-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="dd5d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd5d5-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5d5-103">Ruft die Hyper-V-Websites aus einem Website Wiederherstellungs Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-103">Gets the Hyper-V sites from a Site Recovery vault.</span></span>

## <span data-ttu-id="dd5d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd5d5-104">SYNTAX</span></span>

```
Get-AzureSiteRecoverySite [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dd5d5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd5d5-105">DESCRIPTION</span></span>
<span data-ttu-id="dd5d5-106">Das Cmdlet " **Get-AzureSiteRecoverySite** " Ruft die Hyper-V-Websites in einem Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-106">The **Get-AzureSiteRecoverySite** cmdlet gets the Hyper-V sites in an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="dd5d5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd5d5-107">EXAMPLES</span></span>

### <span data-ttu-id="dd5d5-108">Beispiel 1: Abrufen von Wiederherstellungs Websites</span><span class="sxs-lookup"><span data-stu-id="dd5d5-108">Example 1: Get recovery sites</span></span>
```
PS C:\> Get-AzureSiteRecoverySite
Type                                    Name                                    ID
----                                    ----                                    --
HyperVSite                              RecoverySite07                          f16829b4-5b01-4209-a6cf-8e0aff1fe328
```

<span data-ttu-id="dd5d5-109">Dieser Befehl ruft die Wiederherstellungs Websites für den aktuellen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-109">This command gets the recovery sites for the current vault.</span></span>

## <span data-ttu-id="dd5d5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd5d5-110">PARAMETERS</span></span>

### <span data-ttu-id="dd5d5-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="dd5d5-111">-Profile</span></span>
<span data-ttu-id="dd5d5-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dd5d5-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dd5d5-114">-Vault</span><span class="sxs-lookup"><span data-stu-id="dd5d5-114">-Vault</span></span>
<span data-ttu-id="dd5d5-115">Gibt einen Tresor an, für den Websites abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-115">Specifies a vault for which to get sites.</span></span>
<span data-ttu-id="dd5d5-116">Verwenden Sie das Cmdlet **Get-AzureSiteRecoveryVault** , um ein **ASRVault** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-116">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5d5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5d5-117">CommonParameters</span></span>
<span data-ttu-id="dd5d5-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5d5-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd5d5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5d5-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd5d5-120">INPUTS</span></span>

## <span data-ttu-id="dd5d5-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd5d5-121">OUTPUTS</span></span>

## <span data-ttu-id="dd5d5-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd5d5-122">NOTES</span></span>

## <span data-ttu-id="dd5d5-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd5d5-123">RELATED LINKS</span></span>

[<span data-ttu-id="dd5d5-124">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="dd5d5-124">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="dd5d5-125">Neu – AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="dd5d5-125">New-AzureSiteRecoverySite</span></span>](./New-AzureSiteRecoverySite.md)


