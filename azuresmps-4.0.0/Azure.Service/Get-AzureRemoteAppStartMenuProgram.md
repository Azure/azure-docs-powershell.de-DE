---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: FCDEA955-EB64-4EEA-9F4A-04E2C1F0A831
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83664e8be9241782e42d7ba7634691668ed575f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006521"
---
# <span data-ttu-id="73792-101">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="73792-101">Get-AzureRemoteAppStartMenuProgram</span></span>

## <span data-ttu-id="73792-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73792-102">SYNOPSIS</span></span>
<span data-ttu-id="73792-103">Listet die Start Menü Programme in einer Azure RemoteApp-Sammlung auf.</span><span class="sxs-lookup"><span data-stu-id="73792-103">Lists the Start Menu programs in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="73792-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73792-104">SYNTAX</span></span>

```
Get-AzureRemoteAppStartMenuProgram [-CollectionName] <String> [[-ProgramName] <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="73792-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73792-105">DESCRIPTION</span></span>
<span data-ttu-id="73792-106">Das Cmdlet " **Get-AzureRemoteAppStartMenuProgram** " listet die Startmenü-Programme im Vorlagenbild auf, die von einer Azure RemoteApp-Sammlung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73792-106">The **Get-AzureRemoteAppStartMenuProgram** cmdlet lists the Start Menu programs in the template image that an Azure RemoteApp collection uses.</span></span>

## <span data-ttu-id="73792-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73792-107">EXAMPLES</span></span>

### <span data-ttu-id="73792-108">Beispiel 1: Auflisten der Start Menü Programme für eine Sammlung</span><span class="sxs-lookup"><span data-stu-id="73792-108">Example 1: List the Start Menu programs for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppStartMenuProgram -CollectionName "ContosoApps"
```

<span data-ttu-id="73792-109">Dieser Befehl gibt die Liste der Start Menü Programme für die ContosoApps-Sammlung zurück.</span><span class="sxs-lookup"><span data-stu-id="73792-109">This command returns the list of Start Menu programs for the ContosoApps collection.</span></span>

## <span data-ttu-id="73792-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="73792-110">PARAMETERS</span></span>

### <span data-ttu-id="73792-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="73792-111">-CollectionName</span></span>
<span data-ttu-id="73792-112">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="73792-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="73792-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="73792-113">-Profile</span></span>
<span data-ttu-id="73792-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="73792-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73792-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="73792-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="73792-116">-Programmname</span><span class="sxs-lookup"><span data-stu-id="73792-116">-ProgramName</span></span>
<span data-ttu-id="73792-117">Gibt den Namen des Programms an, für das Informationen aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="73792-117">Specifies the name of a program for which to list information.</span></span>

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

### <span data-ttu-id="73792-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73792-118">CommonParameters</span></span>
<span data-ttu-id="73792-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73792-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73792-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73792-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73792-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73792-121">INPUTS</span></span>

## <span data-ttu-id="73792-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73792-122">OUTPUTS</span></span>

## <span data-ttu-id="73792-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="73792-123">NOTES</span></span>

## <span data-ttu-id="73792-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73792-124">RELATED LINKS</span></span>

[<span data-ttu-id="73792-125">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="73792-125">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)


