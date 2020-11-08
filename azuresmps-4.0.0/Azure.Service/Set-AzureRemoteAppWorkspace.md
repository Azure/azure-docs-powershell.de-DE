---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006257"
---
# <span data-ttu-id="6e79b-101">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="6e79b-101">Set-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="6e79b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e79b-102">SYNOPSIS</span></span>
<span data-ttu-id="6e79b-103">Legt die Eigenschaften eines Azure RemoteApp-Arbeitsbereichs fest.</span><span class="sxs-lookup"><span data-stu-id="6e79b-103">Sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="6e79b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e79b-104">SYNTAX</span></span>

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6e79b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e79b-105">DESCRIPTION</span></span>
<span data-ttu-id="6e79b-106">Das Cmdlet " **Set-AzureRemoteAppWorkspace** " legt die Eigenschaften eines Azure RemoteApp-Arbeitsbereichs fest.</span><span class="sxs-lookup"><span data-stu-id="6e79b-106">The **Set-AzureRemoteAppWorkspace** cmdlet sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="6e79b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e79b-107">EXAMPLES</span></span>

### <span data-ttu-id="6e79b-108">Beispiel 1: Einrichten des Arbeitsbereichs namens</span><span class="sxs-lookup"><span data-stu-id="6e79b-108">Example 1: Set the workspace name</span></span>
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

<span data-ttu-id="6e79b-109">Mit diesem Befehl wird der Azure RemoteApp-Arbeitsbereichsname auf contoso-Arbeitsanwendungen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e79b-109">This command sets the Azure RemoteApp workspace name to Contoso Work Applications.</span></span>

## <span data-ttu-id="6e79b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e79b-110">PARAMETERS</span></span>

### <span data-ttu-id="6e79b-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="6e79b-111">-Profile</span></span>
<span data-ttu-id="6e79b-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6e79b-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6e79b-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6e79b-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6e79b-114">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6e79b-114">-WorkspaceName</span></span>
<span data-ttu-id="6e79b-115">Gibt den Namen des Azure RemoteApp-Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="6e79b-115">Specifies the name of the Azure RemoteApp workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e79b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e79b-116">CommonParameters</span></span>
<span data-ttu-id="6e79b-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e79b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e79b-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e79b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e79b-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e79b-119">INPUTS</span></span>

## <span data-ttu-id="6e79b-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e79b-120">OUTPUTS</span></span>

## <span data-ttu-id="6e79b-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e79b-121">NOTES</span></span>
* <span data-ttu-id="6e79b-122">Alle Azure RemoteApp-Auflistungen für ein angegebenes Abonnement sind in einem freigegebenen Arbeitsbereich vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6e79b-122">All Azure RemoteApp collections for a specified subscription exist within a shared workspace.</span></span>

## <span data-ttu-id="6e79b-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e79b-123">RELATED LINKS</span></span>

[<span data-ttu-id="6e79b-124">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="6e79b-124">Get-AzureRemoteAppWorkspace</span></span>](./Get-AzureRemoteAppWorkspace.md)


