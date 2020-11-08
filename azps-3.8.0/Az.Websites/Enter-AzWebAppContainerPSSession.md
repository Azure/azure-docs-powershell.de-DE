---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004392"
---
# <span data-ttu-id="fbf3a-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="fbf3a-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="fbf3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fbf3a-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf3a-103">Öffnet eine PowerShell-Remotesitzung in dem Windows-Container, der in einer bestimmten Website oder in einem bestimmten Steckplatz und einer gegebenen Ressourcengruppe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fbf3a-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="fbf3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbf3a-104">SYNTAX</span></span>

### <span data-ttu-id="fbf3a-105">S1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="fbf3a-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbf3a-106">S2</span><span class="sxs-lookup"><span data-stu-id="fbf3a-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbf3a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbf3a-107">DESCRIPTION</span></span>
<span data-ttu-id="fbf3a-108">Öffnet eine PowerShell-Remotesitzung in dem Windows-Container, der in einer bestimmten Website oder in einem bestimmten Steckplatz und einer gegebenen Ressourcengruppe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fbf3a-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="fbf3a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbf3a-109">EXAMPLES</span></span>

### <span data-ttu-id="fbf3a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fbf3a-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="fbf3a-111">Mit diesem Befehl wird eine Remote-PowerShell-Sitzung in der Windows-Container-App ContosoASP</span><span class="sxs-lookup"><span data-stu-id="fbf3a-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="fbf3a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbf3a-112">PARAMETERS</span></span>

### <span data-ttu-id="fbf3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf3a-113">-DefaultProfile</span></span>
<span data-ttu-id="fbf3a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fbf3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbf3a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fbf3a-115">-Force</span></span>
<span data-ttu-id="fbf3a-116">Erstellen Sie die PowerShell-Sitzung ohne Aufforderung zur Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="fbf3a-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fbf3a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fbf3a-117">-Name</span></span>
<span data-ttu-id="fbf3a-118">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="fbf3a-118">The name of the web app.</span></span>

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

### <span data-ttu-id="fbf3a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbf3a-119">-PassThru</span></span>
<span data-ttu-id="fbf3a-120">Zurückgeben eines Werts, der auf Erfolg oder Fehler hinweist</span><span class="sxs-lookup"><span data-stu-id="fbf3a-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="fbf3a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf3a-121">-ResourceGroupName</span></span>
<span data-ttu-id="fbf3a-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fbf3a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="fbf3a-123">-Slotname</span><span class="sxs-lookup"><span data-stu-id="fbf3a-123">-SlotName</span></span>
<span data-ttu-id="fbf3a-124">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="fbf3a-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf3a-125">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="fbf3a-125">-WebApp</span></span>
<span data-ttu-id="fbf3a-126">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="fbf3a-126">The web app object</span></span>

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

### <span data-ttu-id="fbf3a-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fbf3a-127">-Confirm</span></span>
<span data-ttu-id="fbf3a-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbf3a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbf3a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbf3a-129">-WhatIf</span></span>
<span data-ttu-id="fbf3a-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbf3a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbf3a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbf3a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbf3a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf3a-132">CommonParameters</span></span>
<span data-ttu-id="fbf3a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbf3a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf3a-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbf3a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf3a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fbf3a-135">INPUTS</span></span>

### <span data-ttu-id="fbf3a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fbf3a-136">System.String</span></span>

### <span data-ttu-id="fbf3a-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="fbf3a-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fbf3a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fbf3a-138">OUTPUTS</span></span>

### <span data-ttu-id="fbf3a-139">System. void</span><span class="sxs-lookup"><span data-stu-id="fbf3a-139">System.Void</span></span>

## <span data-ttu-id="fbf3a-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="fbf3a-140">NOTES</span></span>

## <span data-ttu-id="fbf3a-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fbf3a-141">RELATED LINKS</span></span>
