---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 88eaf66ea8584913c7816fd12be19509aec49de5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003125"
---
# <span data-ttu-id="fdb00-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fdb00-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="fdb00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fdb00-102">SYNOPSIS</span></span>

## <span data-ttu-id="fdb00-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdb00-103">SYNTAX</span></span>

### <span data-ttu-id="fdb00-104">S1</span><span class="sxs-lookup"><span data-stu-id="fdb00-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb00-105">S2</span><span class="sxs-lookup"><span data-stu-id="fdb00-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb00-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdb00-106">DESCRIPTION</span></span>
<span data-ttu-id="fdb00-107">Mit dem Cmdlet **Remove-AzWebAppSlot** wird ein Azure Web App-Steckplatz entfernt, vorausgesetzt, die Ressourcengruppe und der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="fdb00-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="fdb00-108">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="fdb00-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="fdb00-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdb00-109">EXAMPLES</span></span>

### <span data-ttu-id="fdb00-110">Beispiel 1: Entfernen eines Web App-Slots</span><span class="sxs-lookup"><span data-stu-id="fdb00-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="fdb00-111">Mit diesem Befehl wird der Steckplatz mit dem Namen "Slot001" entfernt, der Web App-ContosoSite zugeordnet ist, die zu der Ressourcengruppe "Default-Web-westus" gehört.</span><span class="sxs-lookup"><span data-stu-id="fdb00-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="fdb00-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdb00-112">PARAMETERS</span></span>

### <span data-ttu-id="fdb00-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdb00-113">-AsJob</span></span>
<span data-ttu-id="fdb00-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fdb00-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb00-115">-DefaultProfile</span></span>
<span data-ttu-id="fdb00-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fdb00-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb00-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fdb00-117">-Force</span></span>
<span data-ttu-id="fdb00-118">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="fdb00-118">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb00-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fdb00-119">-Name</span></span>
<span data-ttu-id="fdb00-120">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="fdb00-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb00-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb00-121">-ResourceGroupName</span></span>
<span data-ttu-id="fdb00-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="fdb00-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb00-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="fdb00-123">-Slot</span></span>
<span data-ttu-id="fdb00-124">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="fdb00-124">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb00-125">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="fdb00-125">-WebApp</span></span>
<span data-ttu-id="fdb00-126">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="fdb00-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb00-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fdb00-127">-Confirm</span></span>
<span data-ttu-id="fdb00-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fdb00-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb00-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb00-129">-WhatIf</span></span>
<span data-ttu-id="fdb00-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fdb00-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdb00-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fdb00-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb00-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb00-132">CommonParameters</span></span>
<span data-ttu-id="fdb00-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb00-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb00-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb00-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb00-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fdb00-135">INPUTS</span></span>

### <span data-ttu-id="fdb00-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fdb00-136">System.String</span></span>

### <span data-ttu-id="fdb00-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="fdb00-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fdb00-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fdb00-138">OUTPUTS</span></span>

### <span data-ttu-id="fdb00-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fdb00-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="fdb00-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="fdb00-140">NOTES</span></span>

## <span data-ttu-id="fdb00-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fdb00-141">RELATED LINKS</span></span>

[<span data-ttu-id="fdb00-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fdb00-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="fdb00-143">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fdb00-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="fdb00-144">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fdb00-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="fdb00-145">Satz-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fdb00-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="fdb00-146">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fdb00-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="fdb00-147">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fdb00-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="fdb00-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fdb00-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
