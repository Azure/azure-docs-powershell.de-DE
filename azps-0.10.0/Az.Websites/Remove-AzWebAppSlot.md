---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 04813b04d3d2499de549655edb6398550ce25536
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842715"
---
# <span data-ttu-id="f9906-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f9906-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="f9906-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9906-102">SYNOPSIS</span></span>

## <span data-ttu-id="f9906-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9906-103">SYNTAX</span></span>

### <span data-ttu-id="f9906-104">S1</span><span class="sxs-lookup"><span data-stu-id="f9906-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9906-105">S2</span><span class="sxs-lookup"><span data-stu-id="f9906-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9906-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9906-106">DESCRIPTION</span></span>
<span data-ttu-id="f9906-107">Mit dem Cmdlet **Remove-AzWebAppSlot** wird ein Azure Web App-Steckplatz entfernt, vorausgesetzt, die Ressourcengruppe und der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="f9906-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="f9906-108">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="f9906-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="f9906-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9906-109">EXAMPLES</span></span>

### <span data-ttu-id="f9906-110">Beispiel 1: Entfernen eines Web App-Slots</span><span class="sxs-lookup"><span data-stu-id="f9906-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="f9906-111">Mit diesem Befehl wird der Steckplatz mit dem Namen "Slot001" entfernt, der Web App-ContosoSite zugeordnet ist, die zu der Ressourcengruppe "Default-Web-westus" gehört.</span><span class="sxs-lookup"><span data-stu-id="f9906-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f9906-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9906-112">PARAMETERS</span></span>

### <span data-ttu-id="f9906-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9906-113">-DefaultProfile</span></span>
<span data-ttu-id="f9906-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9906-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9906-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f9906-115">-Force</span></span>
<span data-ttu-id="f9906-116">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="f9906-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="f9906-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f9906-117">-Name</span></span>
<span data-ttu-id="f9906-118">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="f9906-118">WebApp Name</span></span>

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

### <span data-ttu-id="f9906-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9906-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9906-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f9906-120">Resource Group Name</span></span>

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

### <span data-ttu-id="f9906-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="f9906-121">-Slot</span></span>
<span data-ttu-id="f9906-122">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="f9906-122">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9906-123">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="f9906-123">-WebApp</span></span>
<span data-ttu-id="f9906-124">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="f9906-124">WebApp Object</span></span>

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

### <span data-ttu-id="f9906-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9906-125">-Confirm</span></span>
<span data-ttu-id="f9906-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9906-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9906-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9906-127">-WhatIf</span></span>
<span data-ttu-id="f9906-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9906-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9906-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9906-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="f9906-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9906-130">-AsJob</span></span>
<span data-ttu-id="f9906-131">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f9906-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9906-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9906-132">CommonParameters</span></span>
<span data-ttu-id="f9906-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9906-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9906-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9906-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9906-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9906-135">INPUTS</span></span>

### <span data-ttu-id="f9906-136">Website</span><span class="sxs-lookup"><span data-stu-id="f9906-136">Site</span></span>
<span data-ttu-id="f9906-137">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f9906-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f9906-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9906-138">OUTPUTS</span></span>

### <span data-ttu-id="f9906-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f9906-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="f9906-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9906-140">NOTES</span></span>

## <span data-ttu-id="f9906-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9906-141">RELATED LINKS</span></span>

[<span data-ttu-id="f9906-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f9906-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="f9906-143">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f9906-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="f9906-144">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f9906-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="f9906-145">Satz-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f9906-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="f9906-146">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f9906-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="f9906-147">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f9906-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="f9906-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f9906-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
