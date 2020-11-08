---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 035B294E-6A1B-41E9-ACFF-D66F9C1A0B11
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9218862bb1e61abe548a94ed5297a6ce69237d54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005825"
---
# <span data-ttu-id="bec9a-101">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="bec9a-101">Get-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="bec9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bec9a-102">SYNOPSIS</span></span>
<span data-ttu-id="bec9a-103">Ruft Informationen zu einem Azure RemoteApp-Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="bec9a-103">Retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="bec9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bec9a-104">SYNTAX</span></span>

```
Get-AzureRemoteAppWorkspace [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bec9a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bec9a-105">DESCRIPTION</span></span>
<span data-ttu-id="bec9a-106">Das Cmdlet " **Get-AzureRemoteAppWorkspace** " Ruft Informationen zu einem Azure RemoteApp-Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="bec9a-106">The **Get-AzureRemoteAppWorkspace** cmdlet retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="bec9a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bec9a-107">EXAMPLES</span></span>

### <span data-ttu-id="bec9a-108">Beispiel 1: Abrufen von Informationen zu einem Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="bec9a-108">Example 1: Retrieve information about a workspace</span></span>
```
PS C:\> Get-AzureRemoteAppWorkspace
ClientUrl                               EndUserFeedName
---------                               ---------------
https://www.remoteapp.windowsazure.com/ Contoso Work Applications
```

<span data-ttu-id="bec9a-109">Mit diesem Befehl werden Informationen zum Azure RemoteApp-Arbeitsbereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="bec9a-109">This command retrieves information about the Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="bec9a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bec9a-110">PARAMETERS</span></span>

### <span data-ttu-id="bec9a-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="bec9a-111">-Profile</span></span>
<span data-ttu-id="bec9a-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="bec9a-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bec9a-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="bec9a-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bec9a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec9a-114">CommonParameters</span></span>
<span data-ttu-id="bec9a-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec9a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec9a-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec9a-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec9a-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bec9a-117">INPUTS</span></span>

## <span data-ttu-id="bec9a-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bec9a-118">OUTPUTS</span></span>

## <span data-ttu-id="bec9a-119">Notizen</span><span class="sxs-lookup"><span data-stu-id="bec9a-119">NOTES</span></span>

## <span data-ttu-id="bec9a-120">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bec9a-120">RELATED LINKS</span></span>

[<span data-ttu-id="bec9a-121">Satz-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="bec9a-121">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)


