---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 0533864f3fd16e9810e837629782b767fbdc0435
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175208"
---
# <span data-ttu-id="4707f-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4707f-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="4707f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4707f-102">SYNOPSIS</span></span>
<span data-ttu-id="4707f-103">Heben Sie die Registrierung der Windows Virtual Desktop-Anwendungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="4707f-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="4707f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4707f-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4707f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4707f-105">DESCRIPTION</span></span>
<span data-ttu-id="4707f-106">Heben Sie die Registrierung der Windows Virtual Desktop-Anwendungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="4707f-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="4707f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4707f-107">EXAMPLES</span></span>

### <span data-ttu-id="4707f-108">Beispiel 1: Aufheben der Registrierung einer Windows Virtual Desktop-Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="4707f-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="4707f-109">Mit diesem Befehl wird die Registrierung einer Windows Virtual Desktop-Anwendungsgruppe für einen Arbeitsbereich aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="4707f-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="4707f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4707f-110">PARAMETERS</span></span>

### <span data-ttu-id="4707f-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="4707f-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="4707f-112">ResourceGroupName-Pfad</span><span class="sxs-lookup"><span data-stu-id="4707f-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="4707f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4707f-113">-DefaultProfile</span></span>
<span data-ttu-id="4707f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4707f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4707f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4707f-115">-ResourceGroupName</span></span>
<span data-ttu-id="4707f-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="4707f-116">Resource Group Name</span></span>

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

### <span data-ttu-id="4707f-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4707f-117">-SubscriptionId</span></span>
<span data-ttu-id="4707f-118">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="4707f-118">Subscription Id</span></span>

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

### <span data-ttu-id="4707f-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4707f-119">-WorkspaceName</span></span>
<span data-ttu-id="4707f-120">Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="4707f-120">Workspace Name</span></span>

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

### <span data-ttu-id="4707f-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4707f-121">-Confirm</span></span>
<span data-ttu-id="4707f-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4707f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4707f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4707f-123">-WhatIf</span></span>
<span data-ttu-id="4707f-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4707f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4707f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4707f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4707f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4707f-126">CommonParameters</span></span>
<span data-ttu-id="4707f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4707f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4707f-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4707f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4707f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4707f-129">INPUTS</span></span>

## <span data-ttu-id="4707f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4707f-130">OUTPUTS</span></span>

### <span data-ttu-id="4707f-131">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="4707f-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="4707f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="4707f-132">NOTES</span></span>

<span data-ttu-id="4707f-133">Aliase</span><span class="sxs-lookup"><span data-stu-id="4707f-133">ALIASES</span></span>

## <span data-ttu-id="4707f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4707f-134">RELATED LINKS</span></span>

