---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-help.xml
ms.assetid: 02F429EA-FE9A-427F-86B5-C9C4275FD3EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 289cc21b6edd2a841b8121672d838aaa056db4f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005904"
---
# <span data-ttu-id="c5fdf-101">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="c5fdf-101">Copy-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="c5fdf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="c5fdf-103">Kopiert den Benutzerdatenträger eines Benutzers aus einer Azure RemoteApp-Sammlung in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-103">Copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="c5fdf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5fdf-104">SYNTAX</span></span>

```
Copy-AzureRemoteAppUserDisk [-SourceCollectionName] <String> [-DestinationCollectionName] <String>
 [-UserUpn] <String> [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c5fdf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5fdf-105">DESCRIPTION</span></span>
<span data-ttu-id="c5fdf-106">Das Cmdlet **Copy-AzureRemoteAppUserDisk** kopiert den Benutzerdatenträger eines Benutzers aus einer Azure RemoteApp-Sammlung in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-106">The **Copy-AzureRemoteAppUserDisk** cmdlet copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="c5fdf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5fdf-107">EXAMPLES</span></span>

### <span data-ttu-id="c5fdf-108">Beispiel 1: Kopieren eines Benutzer Datenträgers</span><span class="sxs-lookup"><span data-stu-id="c5fdf-108">Example 1: Copy a user disk</span></span>
```
PS C:\> Copy-AzureRemoteAppUserDisk -DestinationCollectionName "Contoso02" -SourceCollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com" -OverwriteExistingUserDisk
```

<span data-ttu-id="c5fdf-109">Mit diesem Befehl wird der Benutzerdatenträger eines Azure Active Directory-Benutzers kopiert, der über den UPN PattiFuller@contoso.com aus der Auflistungs-contoso01 zum Contoso02 der Sammlung verfügt.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-109">This command copies the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01 to the collection Contoso02.</span></span>
<span data-ttu-id="c5fdf-110">Wenn bereits ein Benutzerdatenträger für PattiFuller@contoso.com Contoso02 vorhanden ist, wird dieser durch diesen Befehl überschrieben.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-110">If a user disk for PattiFuller@contoso.com already exists on Contoso02, this command overwrites it.</span></span>

## <span data-ttu-id="c5fdf-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5fdf-111">PARAMETERS</span></span>

### <span data-ttu-id="c5fdf-112">-DestinationCollectionName</span><span class="sxs-lookup"><span data-stu-id="c5fdf-112">-DestinationCollectionName</span></span>
<span data-ttu-id="c5fdf-113">Gibt den Namen der Ziel Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-113">Specifies the name of the destination Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5fdf-114">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="c5fdf-114">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="c5fdf-115">Gibt an, dass mit diesem Cmdlet ein vorhandener Benutzerdatenträger überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-115">Indicates that this cmdlet overwrites an existing user disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5fdf-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="c5fdf-116">-Profile</span></span>
<span data-ttu-id="c5fdf-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5fdf-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5fdf-119">-SourceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c5fdf-119">-SourceCollectionName</span></span>
<span data-ttu-id="c5fdf-120">Gibt den Namen der Quell Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-120">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="c5fdf-121">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="c5fdf-121">-UserUpn</span></span>
<span data-ttu-id="c5fdf-122">Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) des Benutzers an, für den das Cmdlet den Datenträger kopiert.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-122">Specifies the user principal name (UPN) of the user for whom this cmdlet copies the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5fdf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5fdf-123">CommonParameters</span></span>
<span data-ttu-id="c5fdf-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5fdf-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5fdf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5fdf-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5fdf-126">INPUTS</span></span>

## <span data-ttu-id="c5fdf-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5fdf-127">OUTPUTS</span></span>

## <span data-ttu-id="c5fdf-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5fdf-128">NOTES</span></span>

## <span data-ttu-id="c5fdf-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5fdf-129">RELATED LINKS</span></span>

[<span data-ttu-id="c5fdf-130">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="c5fdf-130">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


