---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1ECF6BB5-3751-4DA0-AC6C-A64F15F46D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552c2511a806abb4329860e7c15d8a68b5e03f79
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007619"
---
# <span data-ttu-id="c51ca-101">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="c51ca-101">Remove-WAPackCloudService</span></span>

## <span data-ttu-id="c51ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c51ca-102">SYNOPSIS</span></span>
<span data-ttu-id="c51ca-103">Entfernt Cloud-Dienstobjekte.</span><span class="sxs-lookup"><span data-stu-id="c51ca-103">Removes cloud service objects.</span></span>

## <span data-ttu-id="c51ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c51ca-104">SYNTAX</span></span>

```
Remove-WAPackCloudService -CloudService <CloudService> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c51ca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c51ca-105">DESCRIPTION</span></span>
<span data-ttu-id="c51ca-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="c51ca-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="c51ca-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c51ca-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c51ca-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c51ca-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c51ca-109">Das Cmdlet **Remove-WAPackCloudService** entfernt Cloud-Dienstobjekte.</span><span class="sxs-lookup"><span data-stu-id="c51ca-109">The **Remove-WAPackCloudService** cmdlet removes cloud service objects.</span></span>

## <span data-ttu-id="c51ca-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c51ca-110">EXAMPLES</span></span>

### <span data-ttu-id="c51ca-111">Beispiel 1: Entfernen eines Cloud-Diensts</span><span class="sxs-lookup"><span data-stu-id="c51ca-111">Example 1: Remove a cloud service</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService01"
PS C:\> Remove-WAPackVM -VM $CloudService
```

<span data-ttu-id="c51ca-112">Der erste Befehl ruft den clouddienst mit dem Namen ContosoCloudService01 mit dem Cmdlet **Get-WAPackCloudService** ab und speichert dieses Objekt dann in der $CloudService Variablen.</span><span class="sxs-lookup"><span data-stu-id="c51ca-112">The first command gets the cloud service named ContosoCloudService01 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="c51ca-113">Der zweite Befehl entfernt die cloudservice, die in $CloudService gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c51ca-113">The second command removes the cloudservice stored in $CloudService.</span></span>
<span data-ttu-id="c51ca-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="c51ca-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="c51ca-115">Beispiel 2: Entfernen eines Cloud-Diensts ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="c51ca-115">Example 2: Remove a cloud service without confirmation</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService02"
PS C:\> Remove-WAPackCloudService -VM $CloudService -Force
```

<span data-ttu-id="c51ca-116">Der erste Befehl ruft den clouddienst mit dem Namen ContosoCloudService02 mit dem Cmdlet **Get-WAPackCloudService** ab und speichert dieses Objekt dann in der $CloudService Variablen.</span><span class="sxs-lookup"><span data-stu-id="c51ca-116">The first command gets the cloud service named ContosoCloudService02 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="c51ca-117">Der zweite Befehl entfernt den in $CloudService gespeicherten clouddienst.</span><span class="sxs-lookup"><span data-stu-id="c51ca-117">The second command removes the cloud service stored in $CloudService.</span></span>
<span data-ttu-id="c51ca-118">Dieser Befehl enthält den Parameter *Force* .</span><span class="sxs-lookup"><span data-stu-id="c51ca-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="c51ca-119">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="c51ca-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c51ca-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c51ca-120">PARAMETERS</span></span>

### <span data-ttu-id="c51ca-121">-CloudService</span><span class="sxs-lookup"><span data-stu-id="c51ca-121">-CloudService</span></span>
<span data-ttu-id="c51ca-122">Gibt ein Cloud-Dienstobjekt an.</span><span class="sxs-lookup"><span data-stu-id="c51ca-122">Specifies a cloud service object.</span></span>
<span data-ttu-id="c51ca-123">Verwenden Sie zum Abrufen eines Cloud-Diensts das Cmdlet **Get-WAPackCloudService** .</span><span class="sxs-lookup"><span data-stu-id="c51ca-123">To obtain a cloud service, use the **Get-WAPackCloudService** cmdlet.</span></span>

```yaml
Type: CloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c51ca-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c51ca-124">-Force</span></span>
<span data-ttu-id="c51ca-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c51ca-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c51ca-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c51ca-126">-PassThru</span></span>
<span data-ttu-id="c51ca-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c51ca-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c51ca-128">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c51ca-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c51ca-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="c51ca-129">-Profile</span></span>
<span data-ttu-id="c51ca-130">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c51ca-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c51ca-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c51ca-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c51ca-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c51ca-132">-Confirm</span></span>
<span data-ttu-id="c51ca-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c51ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c51ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c51ca-134">-WhatIf</span></span>
<span data-ttu-id="c51ca-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c51ca-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c51ca-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c51ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c51ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c51ca-137">CommonParameters</span></span>
<span data-ttu-id="c51ca-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c51ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c51ca-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c51ca-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c51ca-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c51ca-140">INPUTS</span></span>

## <span data-ttu-id="c51ca-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c51ca-141">OUTPUTS</span></span>

## <span data-ttu-id="c51ca-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="c51ca-142">NOTES</span></span>

## <span data-ttu-id="c51ca-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c51ca-143">RELATED LINKS</span></span>

[<span data-ttu-id="c51ca-144">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="c51ca-144">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="c51ca-145">Neu – WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="c51ca-145">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)


