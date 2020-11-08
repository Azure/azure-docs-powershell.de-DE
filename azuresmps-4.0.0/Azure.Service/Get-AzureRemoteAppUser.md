---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6F2CC9F-8C95-484D-8676-7DAA5E0AA617
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf2a5cc1390db2a6ae5eb49894a47d1ccf0aca4c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006522"
---
# <span data-ttu-id="10a29-101">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="10a29-101">Get-AzureRemoteAppUser</span></span>

## <span data-ttu-id="10a29-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10a29-102">SYNOPSIS</span></span>
<span data-ttu-id="10a29-103">Listet die Benutzer in einer Azure RemoteApp-Sammlung auf.</span><span class="sxs-lookup"><span data-stu-id="10a29-103">Lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="10a29-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10a29-104">SYNTAX</span></span>

```
Get-AzureRemoteAppUser [-CollectionName] <String> [[-UserUpn] <String>] [-Alias <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="10a29-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10a29-105">DESCRIPTION</span></span>
<span data-ttu-id="10a29-106">Das Cmdlet " **Get-AzureRemoteAppUser** " listet die Benutzer in einer Azure RemoteApp-Sammlung auf.</span><span class="sxs-lookup"><span data-stu-id="10a29-106">The **Get-AzureRemoteAppUser** cmdlet lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="10a29-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10a29-107">EXAMPLES</span></span>

### <span data-ttu-id="10a29-108">Beispiel 1: Auflisten der Benutzer einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="10a29-108">Example 1: List the users of a collection</span></span>
```
PS C:\> Get-AzureRemoteAppUser -CollectionName "Contoso"
```

<span data-ttu-id="10a29-109">Dieser Befehl listet die Benutzer auf, die Zugriff auf die Azure RemoteApp-Sammlung mit dem Namen "Contoso" haben.</span><span class="sxs-lookup"><span data-stu-id="10a29-109">This command lists the users who have access to the Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="10a29-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="10a29-110">PARAMETERS</span></span>

### <span data-ttu-id="10a29-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="10a29-111">-Alias</span></span>
<span data-ttu-id="10a29-112">Gibt einen veröffentlichten Programm-Alias an.</span><span class="sxs-lookup"><span data-stu-id="10a29-112">Specifies a published program alias.</span></span>
<span data-ttu-id="10a29-113">Sie können diesen Parameter nur im pro-App-Veröffentlichungsmodus verwenden.</span><span class="sxs-lookup"><span data-stu-id="10a29-113">You can use this parameter only in per-app publishing mode.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10a29-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="10a29-114">-CollectionName</span></span>
<span data-ttu-id="10a29-115">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="10a29-115">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a29-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="10a29-116">-Profile</span></span>
<span data-ttu-id="10a29-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="10a29-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="10a29-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="10a29-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="10a29-119">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="10a29-119">-UserUpn</span></span>
<span data-ttu-id="10a29-120">Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) eines Benutzers an, für den Informationen aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="10a29-120">Specifies the User Principal Name (UPN) of a user for which to list information.</span></span>
<span data-ttu-id="10a29-121">Beispiel: PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="10a29-121">For example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="10a29-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a29-122">CommonParameters</span></span>
<span data-ttu-id="10a29-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a29-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a29-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10a29-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a29-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10a29-125">INPUTS</span></span>

## <span data-ttu-id="10a29-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10a29-126">OUTPUTS</span></span>

## <span data-ttu-id="10a29-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="10a29-127">NOTES</span></span>

## <span data-ttu-id="10a29-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10a29-128">RELATED LINKS</span></span>

[<span data-ttu-id="10a29-129">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="10a29-129">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="10a29-130">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="10a29-130">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="10a29-131">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="10a29-131">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


