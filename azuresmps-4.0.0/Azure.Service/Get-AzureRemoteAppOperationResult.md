---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006528"
---
# <span data-ttu-id="d24d7-101">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="d24d7-101">Get-AzureRemoteAppOperationResult</span></span>

## <span data-ttu-id="d24d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d24d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d24d7-103">Ruft das Ergebnis eines Azure RemoteApp-Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="d24d7-103">Retrieves the result of an Azure RemoteApp operation.</span></span>

## <span data-ttu-id="d24d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d24d7-104">SYNTAX</span></span>

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d24d7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d24d7-105">DESCRIPTION</span></span>
<span data-ttu-id="d24d7-106">Mit dem Cmdlet **Get-AzureRemoteAppOperationResult** wird das Ergebnis eines Azure-RemoteApp-Vorgangs mit langer Laufzeit abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d24d7-106">The **Get-AzureRemoteAppOperationResult** cmdlet retrieves the result of a long-running Azure RemoteApp operation.</span></span>
<span data-ttu-id="d24d7-107">Azure RemoteApp verwendet langlebige Vorgänge für viele Aktionen, die die Verarbeitung durch den Dienst erfordern und nicht sofort zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="d24d7-107">Azure RemoteApp uses long-running operations for many actions that require processing by the service and cannot return immediately.</span></span>
<span data-ttu-id="d24d7-108">Beispiele für Cmdlets, die nach Verfolgungs-IDs zurückgeben, sind **Update-AzureRemoteAppCollection** , **AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** und andere.</span><span class="sxs-lookup"><span data-stu-id="d24d7-108">Examples of cmdlets that return tracking IDs include **Update-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** , and others.</span></span>

## <span data-ttu-id="d24d7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d24d7-109">EXAMPLES</span></span>

### <span data-ttu-id="d24d7-110">Beispiel 1: Verwenden einer Tracking-ID zum Abrufen eines Vorgangs Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="d24d7-110">Example 1: Use a tracking ID to get an operation result</span></span>
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

<span data-ttu-id="d24d7-111">Dieser Befehl speichert die nach Verfolgungs-ID, die von einem Azure RemoteApp-Vorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d24d7-111">This command saves the tracking ID returned from an Azure RemoteApp operation.</span></span>
<span data-ttu-id="d24d7-112">Die Tracking-ID wird im folgenden Befehl an **Get-AzureRemoteAppOperationResult** übergeben.</span><span class="sxs-lookup"><span data-stu-id="d24d7-112">The tracking ID is passed to **Get-AzureRemoteAppOperationResult** in the command that follows.</span></span>

## <span data-ttu-id="d24d7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d24d7-113">PARAMETERS</span></span>

### <span data-ttu-id="d24d7-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="d24d7-114">-Profile</span></span>
<span data-ttu-id="d24d7-115">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d24d7-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d24d7-116">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d24d7-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d24d7-117">-Tracking-Nummer</span><span class="sxs-lookup"><span data-stu-id="d24d7-117">-TrackingId</span></span>
<span data-ttu-id="d24d7-118">Gibt die nach Verfolgungs-ID eines Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="d24d7-118">Specifies the tracking ID of an operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d24d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24d7-119">CommonParameters</span></span>
<span data-ttu-id="d24d7-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d24d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24d7-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d24d7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24d7-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d24d7-122">INPUTS</span></span>

## <span data-ttu-id="d24d7-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d24d7-123">OUTPUTS</span></span>

## <span data-ttu-id="d24d7-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="d24d7-124">NOTES</span></span>

## <span data-ttu-id="d24d7-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d24d7-125">RELATED LINKS</span></span>

[<span data-ttu-id="d24d7-126">Trennen-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="d24d7-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="d24d7-127">Satz-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="d24d7-127">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)

[<span data-ttu-id="d24d7-128">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d24d7-128">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


