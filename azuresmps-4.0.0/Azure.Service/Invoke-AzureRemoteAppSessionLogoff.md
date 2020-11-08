---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 87163619-DEA4-4183-BB11-2D7B16F4BE8A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee4e094c1e38c54b1f9ad4e78723ec49fff1f75b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006453"
---
# <span data-ttu-id="452f5-101">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="452f5-101">Invoke-AzureRemoteAppSessionLogoff</span></span>

## <span data-ttu-id="452f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="452f5-102">SYNOPSIS</span></span>
<span data-ttu-id="452f5-103">Meldet eine Azure RemoteApp-Sitzung sofort ab.</span><span class="sxs-lookup"><span data-stu-id="452f5-103">Logs off an Azure RemoteApp session immediately.</span></span>

## <span data-ttu-id="452f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="452f5-104">SYNTAX</span></span>

```
Invoke-AzureRemoteAppSessionLogoff [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="452f5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="452f5-105">DESCRIPTION</span></span>
<span data-ttu-id="452f5-106">Das Cmdlet **Invoke-AzureRemoteAppSessionLogoff** meldet einen Benutzer sofort aus einer Remotesitzung ab, die in Azure RemoteApp ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="452f5-106">The **Invoke-AzureRemoteAppSessionLogoff** cmdlet immediately logs off a user from a remote session running in Azure RemoteApp.</span></span>

## <span data-ttu-id="452f5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="452f5-107">EXAMPLES</span></span>

### <span data-ttu-id="452f5-108">Beispiel 1: Abmelden eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="452f5-108">Example 1: Log off a user</span></span>
```
PS C:\> Invoke-AzureRemoteAppSessionLogoff -CollectionName ContosoApps -UserUpn PattiFuller@contoso.com
```

<span data-ttu-id="452f5-109">Mit diesem Befehl wird der Benutzer, dessen UPN lautet, abgemeldet PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="452f5-109">This command logs off the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="452f5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="452f5-110">PARAMETERS</span></span>

### <span data-ttu-id="452f5-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="452f5-111">-CollectionName</span></span>
<span data-ttu-id="452f5-112">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="452f5-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="452f5-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="452f5-113">-Profile</span></span>
<span data-ttu-id="452f5-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="452f5-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="452f5-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="452f5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="452f5-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="452f5-116">-UserUpn</span></span>
<span data-ttu-id="452f5-117">Gibt an Sie den Benutzerprinzipalnamen (User Principal Name, UPN) eines Benutzers ein, beispielsweise PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="452f5-117">Specifes the user Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="452f5-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="452f5-118">-Confirm</span></span>
<span data-ttu-id="452f5-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="452f5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="452f5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="452f5-120">-WhatIf</span></span>
<span data-ttu-id="452f5-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="452f5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="452f5-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="452f5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="452f5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="452f5-123">CommonParameters</span></span>
<span data-ttu-id="452f5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="452f5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="452f5-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="452f5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="452f5-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="452f5-126">INPUTS</span></span>

## <span data-ttu-id="452f5-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="452f5-127">OUTPUTS</span></span>

## <span data-ttu-id="452f5-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="452f5-128">NOTES</span></span>

## <span data-ttu-id="452f5-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="452f5-129">RELATED LINKS</span></span>

[<span data-ttu-id="452f5-130">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="452f5-130">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="452f5-131">Trennen-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="452f5-131">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="452f5-132">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="452f5-132">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)


