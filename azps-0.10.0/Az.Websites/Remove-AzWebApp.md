---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 40b14128ec2a1dc48cf098a2c0427728c34c7e22
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842727"
---
# <span data-ttu-id="d0202-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0202-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="d0202-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d0202-102">SYNOPSIS</span></span>
<span data-ttu-id="d0202-103">Entfernt eine Azure Web-App.</span><span class="sxs-lookup"><span data-stu-id="d0202-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="d0202-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0202-104">SYNTAX</span></span>

### <span data-ttu-id="d0202-105">S1</span><span class="sxs-lookup"><span data-stu-id="d0202-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0202-106">S2</span><span class="sxs-lookup"><span data-stu-id="d0202-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0202-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0202-107">DESCRIPTION</span></span>
<span data-ttu-id="d0202-108">Das Cmdlet **Remove-AzWebApp** entfernt eine Azure Web App, die die Ressourcengruppe und den Namen der Web App bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="d0202-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="d0202-109">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="d0202-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="d0202-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0202-110">EXAMPLES</span></span>

### <span data-ttu-id="d0202-111">Beispiel 1: Entfernen einer Web-App</span><span class="sxs-lookup"><span data-stu-id="d0202-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="d0202-112">Mit diesem Befehl wird die Azure Web App mit dem Namen ContosoSite entfernt, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="d0202-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d0202-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0202-113">PARAMETERS</span></span>

### <span data-ttu-id="d0202-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0202-114">-DefaultProfile</span></span>
<span data-ttu-id="d0202-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d0202-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0202-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d0202-116">-Force</span></span>
<span data-ttu-id="d0202-117">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="d0202-117">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="d0202-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d0202-118">-Name</span></span>
<span data-ttu-id="d0202-119">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="d0202-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0202-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0202-120">-ResourceGroupName</span></span>
<span data-ttu-id="d0202-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d0202-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0202-122">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="d0202-122">-WebApp</span></span>
<span data-ttu-id="d0202-123">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="d0202-123">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0202-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d0202-124">-Confirm</span></span>
<span data-ttu-id="d0202-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen. Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0202-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0202-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0202-126">-WhatIf</span></span>
<span data-ttu-id="d0202-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0202-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0202-128">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0202-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0202-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0202-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0202-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0202-130">-AsJob</span></span>
<span data-ttu-id="d0202-131">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d0202-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0202-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0202-132">CommonParameters</span></span>
<span data-ttu-id="d0202-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0202-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0202-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0202-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0202-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d0202-135">INPUTS</span></span>

### <span data-ttu-id="d0202-136">Website</span><span class="sxs-lookup"><span data-stu-id="d0202-136">Site</span></span>
<span data-ttu-id="d0202-137">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0202-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d0202-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d0202-138">OUTPUTS</span></span>

## <span data-ttu-id="d0202-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d0202-139">NOTES</span></span>

## <span data-ttu-id="d0202-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d0202-140">RELATED LINKS</span></span>

[<span data-ttu-id="d0202-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0202-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d0202-142">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0202-142">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="d0202-143">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0202-143">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d0202-144">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0202-144">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="d0202-145">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0202-145">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


