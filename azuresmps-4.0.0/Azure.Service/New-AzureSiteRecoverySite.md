---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 43E5EC54-5DF4-4D32-8657-D7039DD04513
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68152b80711544a76abc17f697fe9730d1a6f1bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006098"
---
# <span data-ttu-id="d5101-101">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="d5101-101">New-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="d5101-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5101-102">SYNOPSIS</span></span>
<span data-ttu-id="d5101-103">Erstellt eine Website Wiederherstellungs Website.</span><span class="sxs-lookup"><span data-stu-id="d5101-103">Creates a Site Recovery site.</span></span>

## <span data-ttu-id="d5101-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5101-104">SYNTAX</span></span>

```
New-AzureSiteRecoverySite -Name <String> [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d5101-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5101-105">DESCRIPTION</span></span>
<span data-ttu-id="d5101-106">Das Cmdlet **New-AzureSiteRecoverySite** erstellt eine Azure Site Recovery-Website im aktuellen Tresor.</span><span class="sxs-lookup"><span data-stu-id="d5101-106">The **New-AzureSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="d5101-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5101-107">EXAMPLES</span></span>

### <span data-ttu-id="d5101-108">Beispiel 1: Erstellen einer Website Wiederherstellungs Website</span><span class="sxs-lookup"><span data-stu-id="d5101-108">Example 1: Create a Site Recovery site</span></span>
```
PS C:\> New-AzureSiteRecoverySite -Name "RecoverySite07"
```

<span data-ttu-id="d5101-109">Dieser Befehl erstellt eine Website Wiederherstellungs Website mit dem Namen RecoverySite07.</span><span class="sxs-lookup"><span data-stu-id="d5101-109">This command creates a site recovery site named RecoverySite07.</span></span>

## <span data-ttu-id="d5101-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5101-110">PARAMETERS</span></span>

### <span data-ttu-id="d5101-111">-Name</span><span class="sxs-lookup"><span data-stu-id="d5101-111">-Name</span></span>
<span data-ttu-id="d5101-112">Gibt den Namen der Website an.</span><span class="sxs-lookup"><span data-stu-id="d5101-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5101-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="d5101-113">-Profile</span></span>
<span data-ttu-id="d5101-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d5101-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d5101-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d5101-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5101-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="d5101-116">-Vault</span></span>
<span data-ttu-id="d5101-117">Gibt einen Tresor an, für den die Website erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5101-117">Specifies a vault for which to create the site.</span></span>
<span data-ttu-id="d5101-118">Verwenden Sie das Cmdlet **Get-AzureSiteRecoveryVault** , um ein **ASRVault** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d5101-118">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

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

### <span data-ttu-id="d5101-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5101-119">CommonParameters</span></span>
<span data-ttu-id="d5101-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5101-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5101-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5101-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5101-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5101-122">INPUTS</span></span>

## <span data-ttu-id="d5101-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5101-123">OUTPUTS</span></span>

## <span data-ttu-id="d5101-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5101-124">NOTES</span></span>

## <span data-ttu-id="d5101-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5101-125">RELATED LINKS</span></span>

[<span data-ttu-id="d5101-126">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="d5101-126">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="d5101-127">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="d5101-127">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)


