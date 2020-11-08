---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 636280D6-32C3-48EF-A271-A4E032F8B334
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0dab3720a4680805e16f695a1ab1b2350554e8f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006525"
---
# <span data-ttu-id="36ea6-101">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="36ea6-101">Get-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="36ea6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="36ea6-103">Ruft die Eigenschaften von einem oder mehreren veröffentlichten Azure RemoteApp-Programmen für eine Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="36ea6-103">Retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="36ea6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36ea6-104">SYNTAX</span></span>

### <span data-ttu-id="36ea6-105">FilterByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="36ea6-105">FilterByName (Default)</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-RemoteAppProgram] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="36ea6-106">FilterByAlias</span><span class="sxs-lookup"><span data-stu-id="36ea6-106">FilterByAlias</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="36ea6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36ea6-107">DESCRIPTION</span></span>
<span data-ttu-id="36ea6-108">Mit dem Cmdlet **Get-AzureRemoteAppProgram werden** die Eigenschaften von einem oder mehreren veröffentlichten Azure RemoteApp-Programmen für eine Sammlung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="36ea6-108">The **Get-AzureRemoteAppProgram** cmdlet retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="36ea6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36ea6-109">EXAMPLES</span></span>

### <span data-ttu-id="36ea6-110">Beispiel 1: Abrufen der Eigenschaften eines Programms</span><span class="sxs-lookup"><span data-stu-id="36ea6-110">Example 1: Retrieve the properties of a program</span></span>
```
PS C:\> Get-AzureRemoteAppProgram -CollectionName "ContosoApps" -RemoteAppProgram "Finance App"

Alias                : edc85816-4b9e-4284-b3dc-faedb505f5d9

AvailableToUsers     : True

CommandLineArguments : 

IconPngUris          : Microsoft.Azure.Management.RemoteApp.Models.IconPngUrisType

IconUri              : https://liverdcxstorage.blob.core.windows.net/icons/12345678-1234-1234-1234-123412341234.ico?se=2015-03-01T17%3A29%3A51Z&amp;amp;sr=b&amp;amp;sp=r&amp;amp;sig=abcdCCavbcF%2asY4RascaBauishCasd2FasdBHtasd2BPasdi5dasdD

Name                 : Contoso Finance

Status               : Published

VirtualPath          : %SYSTEMDRIVE%\Program Files (x86)\Contoso Finance\Finance.exe
```

<span data-ttu-id="36ea6-111">Mit diesem Befehl werden die Eigenschaften eines Azure RemoteApp-Programms angezeigt.</span><span class="sxs-lookup"><span data-stu-id="36ea6-111">This command displays the properties of an Azure RemoteApp program.</span></span>
<span data-ttu-id="36ea6-112">Das Programm mit dem Namen Finance-App befindet sich in der Azure RemoteApp-Sammlung mit dem Namen ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="36ea6-112">The program, named Finance App, is in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="36ea6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="36ea6-113">PARAMETERS</span></span>

### <span data-ttu-id="36ea6-114">-Alias</span><span class="sxs-lookup"><span data-stu-id="36ea6-114">-Alias</span></span>
<span data-ttu-id="36ea6-115">Gibt den Alias des Programms an, für das Eigenschaften abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="36ea6-115">Specifies the alias of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByAlias
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ea6-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="36ea6-116">-CollectionName</span></span>
<span data-ttu-id="36ea6-117">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="36ea6-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="36ea6-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="36ea6-118">-Profile</span></span>
<span data-ttu-id="36ea6-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="36ea6-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="36ea6-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="36ea6-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="36ea6-121">-RemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="36ea6-121">-RemoteAppProgram</span></span>
<span data-ttu-id="36ea6-122">Gibt den Namen des Programms an, für das Eigenschaften abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="36ea6-122">Specifies the name of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="36ea6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ea6-123">CommonParameters</span></span>
<span data-ttu-id="36ea6-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36ea6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ea6-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ea6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ea6-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36ea6-126">INPUTS</span></span>

## <span data-ttu-id="36ea6-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36ea6-127">OUTPUTS</span></span>

## <span data-ttu-id="36ea6-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="36ea6-128">NOTES</span></span>

## <span data-ttu-id="36ea6-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36ea6-129">RELATED LINKS</span></span>

[<span data-ttu-id="36ea6-130">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="36ea6-130">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)

[<span data-ttu-id="36ea6-131">Veröffentlichung aufheben – AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="36ea6-131">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


