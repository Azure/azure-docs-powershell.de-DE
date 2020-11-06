---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: a984a9a76a41db93bee96acfa029ca05a30d85f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480733"
---
# <span data-ttu-id="bc51a-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bc51a-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="bc51a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc51a-102">SYNOPSIS</span></span>
<span data-ttu-id="bc51a-103">Entfernt eine Azure Web-App.</span><span class="sxs-lookup"><span data-stu-id="bc51a-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc51a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc51a-104">SYNTAX</span></span>

### <span data-ttu-id="bc51a-105">S1</span><span class="sxs-lookup"><span data-stu-id="bc51a-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc51a-106">S2</span><span class="sxs-lookup"><span data-stu-id="bc51a-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc51a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc51a-107">DESCRIPTION</span></span>
<span data-ttu-id="bc51a-108">Das Cmdlet **Remove-AzureRmWebApp** entfernt eine Azure Web App, die die Ressourcengruppe und den Namen der Web App bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="bc51a-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="bc51a-109">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="bc51a-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="bc51a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc51a-110">EXAMPLES</span></span>

### <span data-ttu-id="bc51a-111">Beispiel 1: Entfernen einer Web-App</span><span class="sxs-lookup"><span data-stu-id="bc51a-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="bc51a-112">Mit diesem Befehl wird die Azure Web App mit dem Namen ContosoSite entfernt, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="bc51a-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="bc51a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc51a-113">PARAMETERS</span></span>

### <span data-ttu-id="bc51a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc51a-114">-DefaultProfile</span></span>
<span data-ttu-id="bc51a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc51a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc51a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bc51a-116">-Force</span></span>
<span data-ttu-id="bc51a-117">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="bc51a-117">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="bc51a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bc51a-118">-Name</span></span>
<span data-ttu-id="bc51a-119">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="bc51a-119">WebApp Name</span></span>

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

### <span data-ttu-id="bc51a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc51a-120">-ResourceGroupName</span></span>
<span data-ttu-id="bc51a-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="bc51a-121">Resource Group Name</span></span>

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

### <span data-ttu-id="bc51a-122">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="bc51a-122">-WebApp</span></span>
<span data-ttu-id="bc51a-123">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="bc51a-123">WebApp Object</span></span>

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

### <span data-ttu-id="bc51a-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bc51a-124">-Confirm</span></span>
<span data-ttu-id="bc51a-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen. Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc51a-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc51a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc51a-126">-WhatIf</span></span>
<span data-ttu-id="bc51a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc51a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc51a-128">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc51a-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc51a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc51a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc51a-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc51a-130">-AsJob</span></span>
<span data-ttu-id="bc51a-131">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bc51a-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc51a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc51a-132">CommonParameters</span></span>
<span data-ttu-id="bc51a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc51a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc51a-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc51a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc51a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc51a-135">INPUTS</span></span>

### <span data-ttu-id="bc51a-136">Website</span><span class="sxs-lookup"><span data-stu-id="bc51a-136">Site</span></span>
<span data-ttu-id="bc51a-137">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bc51a-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bc51a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc51a-138">OUTPUTS</span></span>

## <span data-ttu-id="bc51a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc51a-139">NOTES</span></span>

## <span data-ttu-id="bc51a-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc51a-140">RELATED LINKS</span></span>

[<span data-ttu-id="bc51a-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bc51a-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="bc51a-142">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bc51a-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="bc51a-143">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bc51a-143">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="bc51a-144">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bc51a-144">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="bc51a-145">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bc51a-145">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


