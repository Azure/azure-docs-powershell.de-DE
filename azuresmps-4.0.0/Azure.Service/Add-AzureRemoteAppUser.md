---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A121B341-091D-42AD-B56A-3C75E25A1BF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8383240f9c1db58a6a22f6754f98211580d31a73
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006587"
---
# <span data-ttu-id="a485b-101">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="a485b-101">Add-AzureRemoteAppUser</span></span>

## <span data-ttu-id="a485b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a485b-102">SYNOPSIS</span></span>
<span data-ttu-id="a485b-103">Fügt einen Benutzer zu einer Azure RemoteApp-Sammlung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a485b-103">Adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="a485b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a485b-104">SYNTAX</span></span>

```
Add-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a485b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a485b-105">DESCRIPTION</span></span>
<span data-ttu-id="a485b-106">Mit dem Cmdlet **Add-AzureRemoteAppUser** wird ein Benutzer zu einer Azure RemoteApp-Sammlung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a485b-106">The **Add-AzureRemoteAppUser** cmdlet adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="a485b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a485b-107">EXAMPLES</span></span>

### <span data-ttu-id="a485b-108">Beispiel 1: Hinzufügen eines Benutzers mit einem Microsoft-Konto</span><span class="sxs-lookup"><span data-stu-id="a485b-108">Example 1: Add a user using a Microsoft Account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType MicrosoftAccount -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="a485b-109">Mit diesem Befehl wird das Microsoft PattiFuller@contoso.com -Konto der Sammlung mit dem Namen Contoso hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a485b-109">This command adds the Microsoft Account PattiFuller@contoso.com to the collection named Contoso.</span></span>

### <span data-ttu-id="a485b-110">Beispiel 2: Hinzufügen eines Benutzers mit einem Azure Active Directory-Konto</span><span class="sxs-lookup"><span data-stu-id="a485b-110">Example 2: Add a user using an Azure Active Directory account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="a485b-111">Dieser Befehl fügt der Sammlung mit dem Namen contoso das Azure Active Directory-Konto hinzu PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="a485b-111">This command adds the Azure Active Directory account PattiFuller@contoso.com to the collection named Contoso.</span></span>

## <span data-ttu-id="a485b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a485b-112">PARAMETERS</span></span>

### <span data-ttu-id="a485b-113">-Alias</span><span class="sxs-lookup"><span data-stu-id="a485b-113">-Alias</span></span>
<span data-ttu-id="a485b-114">Gibt einen veröffentlichten Programm-Alias an.</span><span class="sxs-lookup"><span data-stu-id="a485b-114">Specifies a published program alias.</span></span>
<span data-ttu-id="a485b-115">Sie können diesen Parameter nur im pro-App-Veröffentlichungsmodus verwenden.</span><span class="sxs-lookup"><span data-stu-id="a485b-115">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="a485b-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="a485b-116">-CollectionName</span></span>
<span data-ttu-id="a485b-117">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="a485b-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="a485b-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="a485b-118">-Profile</span></span>
<span data-ttu-id="a485b-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a485b-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a485b-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a485b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a485b-121">-Typ</span><span class="sxs-lookup"><span data-stu-id="a485b-121">-Type</span></span>
<span data-ttu-id="a485b-122">Gibt einen Benutzertyp an.</span><span class="sxs-lookup"><span data-stu-id="a485b-122">Specifies a user type.</span></span>
<span data-ttu-id="a485b-123">Die zulässigen Werte für diesen Parameter sind: OrgId oder MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="a485b-123">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

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

### <span data-ttu-id="a485b-124">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="a485b-124">-UserUpn</span></span>
<span data-ttu-id="a485b-125">Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) eines Benutzers an, beispielsweise PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="a485b-125">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="a485b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a485b-126">CommonParameters</span></span>
<span data-ttu-id="a485b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a485b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a485b-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a485b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a485b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a485b-129">INPUTS</span></span>

## <span data-ttu-id="a485b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a485b-130">OUTPUTS</span></span>

## <span data-ttu-id="a485b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a485b-131">NOTES</span></span>

## <span data-ttu-id="a485b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a485b-132">RELATED LINKS</span></span>

[<span data-ttu-id="a485b-133">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="a485b-133">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)

[<span data-ttu-id="a485b-134">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="a485b-134">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


