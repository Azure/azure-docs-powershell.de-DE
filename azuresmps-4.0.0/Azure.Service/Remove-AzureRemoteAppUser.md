---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DE89F1C4-8441-4438-B235-F5E0F726EFF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc3bad916830cb638d13f39964e12dc874f7d9f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006072"
---
# <span data-ttu-id="698d0-101">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="698d0-101">Remove-AzureRemoteAppUser</span></span>

## <span data-ttu-id="698d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="698d0-102">SYNOPSIS</span></span>
<span data-ttu-id="698d0-103">Entfernt einen Benutzer aus einer Azure RemoteApp-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="698d0-103">Removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="698d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="698d0-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="698d0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="698d0-105">DESCRIPTION</span></span>
<span data-ttu-id="698d0-106">Das Cmdlet **Remove-AzureRemoteAppUser** entfernt einen Benutzer aus einer Azure RemoteApp-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="698d0-106">The **Remove-AzureRemoteAppUser** cmdlet removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="698d0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="698d0-107">EXAMPLES</span></span>

### <span data-ttu-id="698d0-108">Beispiel1: Entfernen eines Benutzers aus einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="698d0-108">Example1: Remove a user from a collection</span></span>
```
PS C:\> Remove-AzureRemoteAppUser -CollectionName "Contoso" -Type OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="698d0-109">Mit diesem Befehl wird der Azure ActiveDirectory PattiFuller@contoso.com -Benutzer aus der Contoso-Auflistung entfernt.</span><span class="sxs-lookup"><span data-stu-id="698d0-109">This command removes the Azure ActiveDirectory user PattiFuller@contoso.com from the Contoso collection.</span></span>

## <span data-ttu-id="698d0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="698d0-110">PARAMETERS</span></span>

### <span data-ttu-id="698d0-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="698d0-111">-Alias</span></span>
<span data-ttu-id="698d0-112">Gibt einen veröffentlichten Programm-Alias an.</span><span class="sxs-lookup"><span data-stu-id="698d0-112">Specifies a published program alias.</span></span>
<span data-ttu-id="698d0-113">Sie können diesen Parameter nur im pro-App-Veröffentlichungsmodus verwenden.</span><span class="sxs-lookup"><span data-stu-id="698d0-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="698d0-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="698d0-114">-CollectionName</span></span>
<span data-ttu-id="698d0-115">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="698d0-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="698d0-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="698d0-116">-Profile</span></span>
<span data-ttu-id="698d0-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="698d0-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="698d0-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="698d0-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="698d0-119">-Typ</span><span class="sxs-lookup"><span data-stu-id="698d0-119">-Type</span></span>
<span data-ttu-id="698d0-120">Gibt einen Benutzertyp an.</span><span class="sxs-lookup"><span data-stu-id="698d0-120">Specifies a user type.</span></span>
<span data-ttu-id="698d0-121">Die zulässigen Werte für diesen Parameter sind: OrgId oder MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="698d0-121">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

```yaml
Type: PrincipalProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: OrgId, MicrosoftAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698d0-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="698d0-122">-UserUpn</span></span>
<span data-ttu-id="698d0-123">Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) eines Benutzers an, beispielsweise user@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="698d0-123">Specifies the User Principal Name (UPN) of a user, for example, user@contoso.com.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698d0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698d0-124">CommonParameters</span></span>
<span data-ttu-id="698d0-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="698d0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698d0-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="698d0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698d0-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="698d0-127">INPUTS</span></span>

## <span data-ttu-id="698d0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="698d0-128">OUTPUTS</span></span>

## <span data-ttu-id="698d0-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="698d0-129">NOTES</span></span>

## <span data-ttu-id="698d0-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="698d0-130">RELATED LINKS</span></span>

[<span data-ttu-id="698d0-131">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="698d0-131">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="698d0-132">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="698d0-132">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


