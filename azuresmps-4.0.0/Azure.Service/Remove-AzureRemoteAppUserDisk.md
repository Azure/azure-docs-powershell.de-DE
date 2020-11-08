---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A4E9C9A7-7FD2-4FD5-AB35-CFF717607B44
online version: ''
schema: 2.0.0
ms.openlocfilehash: c6da222e6cbfe02e181e4a863d8ce8d585215bdd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006353"
---
# <span data-ttu-id="7a6fd-101">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="7a6fd-101">Remove-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="7a6fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6fd-103">Entfernt den Benutzerdatenträger eines Benutzers aus einer Azure RemoteApp-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="7a6fd-103">Removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="7a6fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a6fd-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUserDisk [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a6fd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a6fd-105">DESCRIPTION</span></span>
<span data-ttu-id="7a6fd-106">Das Cmdlet **Remove-AzureRemoteAppUserDisk** entfernt den Benutzerdatenträger eines Benutzers aus einer Azure RemoteApp-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="7a6fd-106">The **Remove-AzureRemoteAppUserDisk** cmdlet removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="7a6fd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a6fd-107">EXAMPLES</span></span>

### <span data-ttu-id="7a6fd-108">Beispiel 1: Entfernen eines Benutzer Datenträgers</span><span class="sxs-lookup"><span data-stu-id="7a6fd-108">Example 1: Remove a user disk</span></span>
```
PS C:\> Remove-AzureRemoteAppUserDisk -CollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="7a6fd-109">Mit diesem Befehl wird der Benutzerdatenträger eines Azure Active Directory-Benutzers entfernt, der über den UPN PattiFuller@contoso.com aus der Sammlung contoso01.</span><span class="sxs-lookup"><span data-stu-id="7a6fd-109">This command removes the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01.</span></span>

## <span data-ttu-id="7a6fd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a6fd-110">PARAMETERS</span></span>

### <span data-ttu-id="7a6fd-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="7a6fd-111">-CollectionName</span></span>
<span data-ttu-id="7a6fd-112">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="7a6fd-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="7a6fd-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="7a6fd-113">-Profile</span></span>
<span data-ttu-id="7a6fd-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7a6fd-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7a6fd-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7a6fd-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7a6fd-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="7a6fd-116">-UserUpn</span></span>
<span data-ttu-id="7a6fd-117">Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) des Benutzers an, für den das Cmdlet den Datenträger entfernt.</span><span class="sxs-lookup"><span data-stu-id="7a6fd-117">Specifies the user principal name (UPN) of the user for whom this cmdlet removes the disk.</span></span>

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

### <span data-ttu-id="7a6fd-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7a6fd-118">-Confirm</span></span>
<span data-ttu-id="7a6fd-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a6fd-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a6fd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a6fd-120">-WhatIf</span></span>
<span data-ttu-id="7a6fd-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a6fd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a6fd-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a6fd-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a6fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6fd-123">CommonParameters</span></span>
<span data-ttu-id="7a6fd-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a6fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6fd-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a6fd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6fd-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a6fd-126">INPUTS</span></span>

## <span data-ttu-id="7a6fd-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a6fd-127">OUTPUTS</span></span>

## <span data-ttu-id="7a6fd-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a6fd-128">NOTES</span></span>

## <span data-ttu-id="7a6fd-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a6fd-129">RELATED LINKS</span></span>

[<span data-ttu-id="7a6fd-130">Kopieren-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="7a6fd-130">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)


