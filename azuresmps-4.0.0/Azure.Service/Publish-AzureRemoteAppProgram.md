---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006090"
---
# <span data-ttu-id="fd06e-101">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="fd06e-101">Publish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="fd06e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd06e-102">SYNOPSIS</span></span>
<span data-ttu-id="fd06e-103">Veröffentlicht ein Azure RemoteApp-Programm.</span><span class="sxs-lookup"><span data-stu-id="fd06e-103">Publishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="fd06e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd06e-104">SYNTAX</span></span>

### <span data-ttu-id="fd06e-105">APP-ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd06e-105">App Id (Default)</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fd06e-106">App-Pfad</span><span class="sxs-lookup"><span data-stu-id="fd06e-106">App Path</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fd06e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd06e-107">DESCRIPTION</span></span>
<span data-ttu-id="fd06e-108">Das Cmdlet **Publish-AzureRemoteAppProgram** veröffentlicht ein Azure RemoteApp-Programm, das für Benutzer der Azure RemoteApp-Sammlung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fd06e-108">The **Publish-AzureRemoteAppProgram** cmdlet publishes an Azure RemoteApp program, which makes it available to users of the Azure RemoteApp collection.</span></span>

## <span data-ttu-id="fd06e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd06e-109">EXAMPLES</span></span>

### <span data-ttu-id="fd06e-110">Beispiel 1: Veröffentlichen eines Programms in einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="fd06e-110">Example 1: Publish a program in a collection</span></span>
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

<span data-ttu-id="fd06e-111">Dieser Befehl veröffentlicht das Programm in der ContosoApps-Sammlung mit dem angegebenen *StartMenuAppId* , um das Programm zum Startmenü hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fd06e-111">This command publishes the program in the ContosoApps collection with the specified *StartMenuAppId* to add the program to the Start Menu.</span></span>
<span data-ttu-id="fd06e-112">Die veröffentlichte APP hat den Anzeigenamen "Finance-App".</span><span class="sxs-lookup"><span data-stu-id="fd06e-112">The published app will have a display name of "Finance App".</span></span>

## <span data-ttu-id="fd06e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd06e-113">PARAMETERS</span></span>

### <span data-ttu-id="fd06e-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="fd06e-114">-CollectionName</span></span>
<span data-ttu-id="fd06e-115">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="fd06e-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="fd06e-116">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="fd06e-116">-CommandLine</span></span>
<span data-ttu-id="fd06e-117">Gibt Befehlszeilenargumente für das Programm an, das dieses Cmdlet veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="fd06e-117">Specifies command-line arguments for the program that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="fd06e-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fd06e-118">-DisplayName</span></span>
<span data-ttu-id="fd06e-119">Gibt den benutzerfreundlichen Anzeigenamen des Azure RemoteApp-Programms an.</span><span class="sxs-lookup"><span data-stu-id="fd06e-119">Specifies the user-friendly display name of the Azure RemoteApp program.</span></span>
<span data-ttu-id="fd06e-120">Benutzer sehen dies als den Namen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="fd06e-120">Users see this as the name of the application.</span></span>

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

### <span data-ttu-id="fd06e-121">-Filevirtualpath</span><span class="sxs-lookup"><span data-stu-id="fd06e-121">-FileVirtualPath</span></span>
<span data-ttu-id="fd06e-122">Gibt den Pfad des Programms innerhalb des Vorlagenbilds des Programms an.</span><span class="sxs-lookup"><span data-stu-id="fd06e-122">Specifies the path of the program within the template image of the program.</span></span>

```yaml
Type: String
Parameter Sets: App Path
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd06e-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="fd06e-123">-Profile</span></span>
<span data-ttu-id="fd06e-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="fd06e-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fd06e-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="fd06e-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fd06e-126">-StartMenuAppId</span><span class="sxs-lookup"><span data-stu-id="fd06e-126">-StartMenuAppId</span></span>
<span data-ttu-id="fd06e-127">Gibt eine GUID an, die dieses Cmdlet verwendet, um das Programm dem Startmenü hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fd06e-127">Specifies a GUID that this cmdlet uses to add the program to the Start Menu.</span></span>

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd06e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd06e-128">CommonParameters</span></span>
<span data-ttu-id="fd06e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd06e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd06e-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd06e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd06e-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd06e-131">INPUTS</span></span>

## <span data-ttu-id="fd06e-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd06e-132">OUTPUTS</span></span>

## <span data-ttu-id="fd06e-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd06e-133">NOTES</span></span>

## <span data-ttu-id="fd06e-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd06e-134">RELATED LINKS</span></span>

[<span data-ttu-id="fd06e-135">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="fd06e-135">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="fd06e-136">Veröffentlichung aufheben – AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="fd06e-136">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


