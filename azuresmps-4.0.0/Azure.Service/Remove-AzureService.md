---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03107EA1-6ADA-4A3E-B8E1-88788E5F3F37
online version: ''
schema: 2.0.0
ms.openlocfilehash: 21892d129319977897a6855933e3e8542460a4a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006333"
---
# <span data-ttu-id="6a4f7-101">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="6a4f7-101">Remove-AzureService</span></span>

## <span data-ttu-id="6a4f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="6a4f7-103">Entfernt den aktuellen clouddienst.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-103">Removes the current cloud service.</span></span>

## <span data-ttu-id="6a4f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a4f7-104">SYNTAX</span></span>

```
Remove-AzureService [-ServiceName <String>] [-Force] [-PassThru] [-DeleteAll] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a4f7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a4f7-105">DESCRIPTION</span></span>
<span data-ttu-id="6a4f7-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6a4f7-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6a4f7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6a4f7-108">Mit dem Cmdlet **Remove-AzureService** wird der aktuelle clouddienst beendet und entfernt, oder der Dienst, der dem angegebenen Dienst-und Abonnement Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-108">The **Remove-AzureService** cmdlet stops and removes the current cloud service, or the service matching the specified service and subscription name.</span></span>

## <span data-ttu-id="6a4f7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a4f7-109">EXAMPLES</span></span>

## <span data-ttu-id="6a4f7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a4f7-110">PARAMETERS</span></span>

### <span data-ttu-id="6a4f7-111">-DeleteAll</span><span class="sxs-lookup"><span data-stu-id="6a4f7-111">-DeleteAll</span></span>
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

### <span data-ttu-id="6a4f7-112">-Force</span><span class="sxs-lookup"><span data-stu-id="6a4f7-112">-Force</span></span>
<span data-ttu-id="6a4f7-113">Entfernt den Dienst ohne Aufforderung zur Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-113">Removes the service without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6a4f7-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a4f7-114">-PassThru</span></span>
<span data-ttu-id="6a4f7-115">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6a4f7-116">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6a4f7-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="6a4f7-117">-Profile</span></span>
<span data-ttu-id="6a4f7-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6a4f7-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6a4f7-120">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6a4f7-120">-ServiceName</span></span>
<span data-ttu-id="6a4f7-121">Gibt den Namen des Diensts an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-121">Specifies the name of the service to be removed.</span></span>
<span data-ttu-id="6a4f7-122">Wenn der Befehl aus einem Dienstverzeichnis ausgeführt wird und kein Name angegeben wird, wird der aktuelle Dienstname verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-122">If the command is run from a service directory and no name is specified, uses the current service name.</span></span>

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

### <span data-ttu-id="6a4f7-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6a4f7-123">-Confirm</span></span>
<span data-ttu-id="6a4f7-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a4f7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a4f7-125">-WhatIf</span></span>
<span data-ttu-id="6a4f7-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a4f7-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a4f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a4f7-128">CommonParameters</span></span>
<span data-ttu-id="6a4f7-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a4f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a4f7-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a4f7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a4f7-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a4f7-131">INPUTS</span></span>

## <span data-ttu-id="6a4f7-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a4f7-132">OUTPUTS</span></span>

## <span data-ttu-id="6a4f7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a4f7-133">NOTES</span></span>

## <span data-ttu-id="6a4f7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a4f7-134">RELATED LINKS</span></span>

[<span data-ttu-id="6a4f7-135">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="6a4f7-135">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="6a4f7-136">Stopp-AzureService</span><span class="sxs-lookup"><span data-stu-id="6a4f7-136">Stop-AzureService</span></span>](./Stop-AzureService.md)

[<span data-ttu-id="6a4f7-137">Anfang-AzureService</span><span class="sxs-lookup"><span data-stu-id="6a4f7-137">Start-AzureService</span></span>](./Start-AzureService.md)


