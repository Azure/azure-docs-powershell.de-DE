---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D39F4C9-F37A-4BBE-BF02-1F036A9FC5E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec095393d68bb6764fa463941f1cd2b9644092f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006044"
---
# <span data-ttu-id="b2281-101">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="b2281-101">Stop-AzureWebsiteJob</span></span>

## <span data-ttu-id="b2281-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2281-102">SYNOPSIS</span></span>
<span data-ttu-id="b2281-103">Beendet einen Web-Job für eine Website.</span><span class="sxs-lookup"><span data-stu-id="b2281-103">Stops a web job for a website.</span></span>

## <span data-ttu-id="b2281-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2281-104">SYNTAX</span></span>

```
Stop-AzureWebsiteJob -JobName <String> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b2281-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2281-105">DESCRIPTION</span></span>
<span data-ttu-id="b2281-106">Das Cmdlet **Stop-AzureWebsiteJob** beendet einen Web-Job für eine Website.</span><span class="sxs-lookup"><span data-stu-id="b2281-106">The **Stop-AzureWebsiteJob** cmdlet stops a web job for a website.</span></span>

## <span data-ttu-id="b2281-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2281-107">EXAMPLES</span></span>

### <span data-ttu-id="b2281-108">Beispiel 1: Beenden eines Web-Auftrags für eine Website</span><span class="sxs-lookup"><span data-stu-id="b2281-108">Example 1: Stop a web job for a website</span></span>
```
PS C:\> Stop-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="b2281-109">Beendet einen Web-Job namens "MyWebJob" für "Meine Website".</span><span class="sxs-lookup"><span data-stu-id="b2281-109">Stops a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="b2281-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2281-110">PARAMETERS</span></span>

### <span data-ttu-id="b2281-111">-Jobname</span><span class="sxs-lookup"><span data-stu-id="b2281-111">-JobName</span></span>
<span data-ttu-id="b2281-112">Der Name des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="b2281-112">The web job name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2281-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b2281-113">-Name</span></span>
<span data-ttu-id="b2281-114">Der Name der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="b2281-114">The name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2281-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2281-115">-PassThru</span></span>
<span data-ttu-id="b2281-116">Gibt einen booleschen Wert zurück, der angibt, dass der Auftrag erfolgreich beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b2281-116">Returns a boolean value indicating that the job stopped successfully.</span></span>
<span data-ttu-id="b2281-117">Standardmäßig gibt dieses Cmdlet keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="b2281-117">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="b2281-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="b2281-118">-Profile</span></span>
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

### <span data-ttu-id="b2281-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="b2281-119">-Slot</span></span>
<span data-ttu-id="b2281-120">Der Steckplatzname der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="b2281-120">The slot name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2281-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2281-121">CommonParameters</span></span>
<span data-ttu-id="b2281-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2281-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2281-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2281-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2281-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2281-124">INPUTS</span></span>

## <span data-ttu-id="b2281-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2281-125">OUTPUTS</span></span>

## <span data-ttu-id="b2281-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2281-126">NOTES</span></span>

## <span data-ttu-id="b2281-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2281-127">RELATED LINKS</span></span>

[<span data-ttu-id="b2281-128">Stopp-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b2281-128">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="b2281-129">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="b2281-129">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="b2281-130">Neu – AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="b2281-130">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="b2281-131">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="b2281-131">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="b2281-132">Anfang-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="b2281-132">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


