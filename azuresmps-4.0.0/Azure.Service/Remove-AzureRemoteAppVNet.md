---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 000B2335-E374-47CC-8165-40AE807C090F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c097884326d1430804f1d577629b62041bfd402b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006352"
---
# <span data-ttu-id="804fa-101">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="804fa-101">Remove-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="804fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="804fa-102">SYNOPSIS</span></span>
<span data-ttu-id="804fa-103">Löscht ein virtuelles Azure RemoteApp-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="804fa-103">Deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="804fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="804fa-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppVNet -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="804fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="804fa-105">DESCRIPTION</span></span>
<span data-ttu-id="804fa-106">Das Cmdlet **Remove-AzureRemoteAppVNet** löscht ein virtuelles Azure RemoteApp-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="804fa-106">The **Remove-AzureRemoteAppVNet** cmdlet deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="804fa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="804fa-107">EXAMPLES</span></span>

### <span data-ttu-id="804fa-108">Beispiel 1: Löschen eines angegebenen virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="804fa-108">Example 1: Delete a specified virtual network</span></span>
```
PS C:\> Remove-AzureRemoteAppVnet -VNetName "ContosoVNet"
```

<span data-ttu-id="804fa-109">Mit diesem Befehl wird das virtuelle Netzwerk mit dem Namen ContosoVNet gelöscht.</span><span class="sxs-lookup"><span data-stu-id="804fa-109">This command deletes the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="804fa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="804fa-110">PARAMETERS</span></span>

### <span data-ttu-id="804fa-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="804fa-111">-Profile</span></span>
<span data-ttu-id="804fa-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="804fa-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="804fa-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="804fa-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="804fa-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="804fa-114">-VNetName</span></span>
<span data-ttu-id="804fa-115">Gibt den Namen des virtuellen Azure RemoteApp-Netzwerks an, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="804fa-115">Specifies the name of the Azure RemoteApp virtual network to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="804fa-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="804fa-116">CommonParameters</span></span>
<span data-ttu-id="804fa-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="804fa-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="804fa-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="804fa-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="804fa-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="804fa-119">INPUTS</span></span>

## <span data-ttu-id="804fa-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="804fa-120">OUTPUTS</span></span>

## <span data-ttu-id="804fa-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="804fa-121">NOTES</span></span>

## <span data-ttu-id="804fa-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="804fa-122">RELATED LINKS</span></span>

[<span data-ttu-id="804fa-123">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="804fa-123">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="804fa-124">Satz-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="804fa-124">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


