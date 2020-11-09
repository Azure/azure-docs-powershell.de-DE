---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297009"
---
# <span data-ttu-id="6ad3f-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="6ad3f-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="6ad3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ad3f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad3f-103">Registrieren einer Windows Virtual Desktop-Anwendungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="6ad3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ad3f-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6ad3f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ad3f-105">DESCRIPTION</span></span>
<span data-ttu-id="6ad3f-106">Registrieren einer Windows Virtual Desktop-Anwendungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="6ad3f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ad3f-107">EXAMPLES</span></span>

### <span data-ttu-id="6ad3f-108">Beispiel 1: Registrieren einer Windows Virtual Desktop-Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="6ad3f-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="6ad3f-109">Mit diesem Befehl wird eine Windows Virtual Desktop-Anwendungsgruppe in einem Arbeitsbereich registriert.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="6ad3f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ad3f-110">PARAMETERS</span></span>

### <span data-ttu-id="6ad3f-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="6ad3f-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="6ad3f-112">ApplicationGroupPath-Pfad</span><span class="sxs-lookup"><span data-stu-id="6ad3f-112">ApplicationGroupPath Path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad3f-113">-DefaultProfile</span></span>
<span data-ttu-id="6ad3f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad3f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad3f-115">-ResourceGroupName</span></span>
<span data-ttu-id="6ad3f-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="6ad3f-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad3f-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="6ad3f-117">-SubscriptionId</span></span>
<span data-ttu-id="6ad3f-118">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="6ad3f-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad3f-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6ad3f-119">-WorkspaceName</span></span>
<span data-ttu-id="6ad3f-120">Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="6ad3f-120">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad3f-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6ad3f-121">-Confirm</span></span>
<span data-ttu-id="6ad3f-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad3f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad3f-123">-WhatIf</span></span>
<span data-ttu-id="6ad3f-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ad3f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad3f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad3f-126">CommonParameters</span></span>
<span data-ttu-id="6ad3f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad3f-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ad3f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad3f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ad3f-129">INPUTS</span></span>

## <span data-ttu-id="6ad3f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ad3f-130">OUTPUTS</span></span>

### <span data-ttu-id="6ad3f-131">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="6ad3f-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="6ad3f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ad3f-132">NOTES</span></span>

<span data-ttu-id="6ad3f-133">Aliase</span><span class="sxs-lookup"><span data-stu-id="6ad3f-133">ALIASES</span></span>

## <span data-ttu-id="6ad3f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ad3f-134">RELATED LINKS</span></span>

