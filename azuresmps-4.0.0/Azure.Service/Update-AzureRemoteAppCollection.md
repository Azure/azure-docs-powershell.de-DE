---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 67890A2A-7922-4E4A-96B4-B58CF532D2DE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a949128309e2777984be0dac33f27b0bc53aab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005943"
---
# <span data-ttu-id="91a5f-101">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="91a5f-101">Update-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="91a5f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="91a5f-103">Aktualisiert eine Azure RemoteApp-Sammlung mit einem neuen Vorlagenbild.</span><span class="sxs-lookup"><span data-stu-id="91a5f-103">Updates an Azure RemoteApp collection with a new template image.</span></span>

## <span data-ttu-id="91a5f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91a5f-104">SYNTAX</span></span>

```
Update-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [[-SubnetName] <String>]
 [-ForceLogoffWhenUpdateComplete] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91a5f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91a5f-105">DESCRIPTION</span></span>
<span data-ttu-id="91a5f-106">Das Cmdlet **Update-AzureRemoteAppCollection** aktualisiert eine Azure RemoteApp-Sammlung mit einem neuen Vorlagenbild.</span><span class="sxs-lookup"><span data-stu-id="91a5f-106">The **Update-AzureRemoteAppCollection** cmdlet updates an Azure RemoteApp collection with a new template image.</span></span>
<span data-ttu-id="91a5f-107">Nach Abschluss des Updates haben Benutzer mit vorhandenen Sitzungen eine Stunde Zeit, um sich abzumelden, bevor Sie automatisch abgemeldet werden. Wenn Sie sich erneut anmelden, stellen Sie eine Verbindung mit der neu aktualisierten Sammlung her.</span><span class="sxs-lookup"><span data-stu-id="91a5f-107">After the update completes, users with existing sessions have one hour to sign out before they are automatically signed out. When they sign in again, they connect to the newly updated collection.</span></span>
<span data-ttu-id="91a5f-108">Wenn Sie erzwingen möchten, dass Benutzer sofort nach der Aktualisierung der Sammlung abgemeldet werden, geben Sie den Parameter *ForceLogoffWhenUpdateComplete* an.</span><span class="sxs-lookup"><span data-stu-id="91a5f-108">To force users to be immediately signed out as soon as the collection is updated, specify the *ForceLogoffWhenUpdateComplete* parameter.</span></span>

## <span data-ttu-id="91a5f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91a5f-109">EXAMPLES</span></span>

## <span data-ttu-id="91a5f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="91a5f-110">PARAMETERS</span></span>

### <span data-ttu-id="91a5f-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="91a5f-111">-CollectionName</span></span>
<span data-ttu-id="91a5f-112">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="91a5f-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="91a5f-113">-ForceLogoffWhenUpdateComplete</span><span class="sxs-lookup"><span data-stu-id="91a5f-113">-ForceLogoffWhenUpdateComplete</span></span>
<span data-ttu-id="91a5f-114">Gibt an, dass Benutzer von diesem Cmdlet nach Abschluss des Updates aus Ihren vorhandenen Sitzungen heraus signiert werden.</span><span class="sxs-lookup"><span data-stu-id="91a5f-114">Indicates that this cmdlet signs users out of their existing sessions as soon as the update is complete.</span></span>
<span data-ttu-id="91a5f-115">Wenn sich Benutzer erneut anmelden, stellen Sie eine Verbindung mit der neu aktualisierten Sammlung her.</span><span class="sxs-lookup"><span data-stu-id="91a5f-115">When users sign in again, they connect to the newly updated collection.</span></span>

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

### <span data-ttu-id="91a5f-116">-Bildname</span><span class="sxs-lookup"><span data-stu-id="91a5f-116">-ImageName</span></span>
<span data-ttu-id="91a5f-117">Gibt den Namen eines Azure RemoteApp-Vorlagenbilds an.</span><span class="sxs-lookup"><span data-stu-id="91a5f-117">Specifies the name of an Azure RemoteApp template image.</span></span>

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

### <span data-ttu-id="91a5f-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="91a5f-118">-Profile</span></span>
<span data-ttu-id="91a5f-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="91a5f-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="91a5f-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="91a5f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="91a5f-121">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="91a5f-121">-SubnetName</span></span>
<span data-ttu-id="91a5f-122">Gibt den Namen des Subnets an, in das die Sammlung verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="91a5f-122">Specifies the name of the subnet into which to move the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91a5f-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91a5f-123">-Confirm</span></span>
<span data-ttu-id="91a5f-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91a5f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91a5f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91a5f-125">-WhatIf</span></span>
<span data-ttu-id="91a5f-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91a5f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91a5f-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91a5f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91a5f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a5f-128">CommonParameters</span></span>
<span data-ttu-id="91a5f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91a5f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a5f-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91a5f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a5f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91a5f-131">INPUTS</span></span>

## <span data-ttu-id="91a5f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91a5f-132">OUTPUTS</span></span>

## <span data-ttu-id="91a5f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="91a5f-133">NOTES</span></span>

## <span data-ttu-id="91a5f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91a5f-134">RELATED LINKS</span></span>

[<span data-ttu-id="91a5f-135">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="91a5f-135">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="91a5f-136">Neu – AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="91a5f-136">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="91a5f-137">Satz-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="91a5f-137">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)


