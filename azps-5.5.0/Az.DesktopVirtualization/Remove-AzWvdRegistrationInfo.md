---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163665"
---
# <span data-ttu-id="f81c7-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="f81c7-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="f81c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f81c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f81c7-103">Entfernen Sie die Registrierungsinformationen für den virtuellen Windows-Desktop.</span><span class="sxs-lookup"><span data-stu-id="f81c7-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="f81c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f81c7-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f81c7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f81c7-105">DESCRIPTION</span></span>
<span data-ttu-id="f81c7-106">Entfernen Sie die Registrierungsinformationen für den virtuellen Windows-Desktop.</span><span class="sxs-lookup"><span data-stu-id="f81c7-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="f81c7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f81c7-107">EXAMPLES</span></span>

### <span data-ttu-id="f81c7-108">Beispiel 1: Löschen eines Tokens für die Registrierung des virtuellen Windows-Desktops</span><span class="sxs-lookup"><span data-stu-id="f81c7-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="f81c7-109">Mit diesem Befehl wird ein Windows Virtual Desktop Registration Token in einem Hostpool gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f81c7-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="f81c7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f81c7-110">PARAMETERS</span></span>

### <span data-ttu-id="f81c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f81c7-111">-DefaultProfile</span></span>
<span data-ttu-id="f81c7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f81c7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f81c7-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f81c7-113">-HostPoolName</span></span>
<span data-ttu-id="f81c7-114">Name des Hostpools</span><span class="sxs-lookup"><span data-stu-id="f81c7-114">Host Pool Name</span></span>

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

### <span data-ttu-id="f81c7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f81c7-115">-ResourceGroupName</span></span>
<span data-ttu-id="f81c7-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f81c7-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f81c7-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f81c7-117">-SubscriptionId</span></span>
<span data-ttu-id="f81c7-118">Hilfe foo 1</span><span class="sxs-lookup"><span data-stu-id="f81c7-118">help foo 1</span></span>

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

### <span data-ttu-id="f81c7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f81c7-119">-Confirm</span></span>
<span data-ttu-id="f81c7-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f81c7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f81c7-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f81c7-121">-WhatIf</span></span>
<span data-ttu-id="f81c7-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f81c7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f81c7-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f81c7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f81c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f81c7-124">CommonParameters</span></span>
<span data-ttu-id="f81c7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f81c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f81c7-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f81c7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f81c7-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f81c7-127">INPUTS</span></span>

## <span data-ttu-id="f81c7-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f81c7-128">OUTPUTS</span></span>

## <span data-ttu-id="f81c7-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f81c7-129">NOTES</span></span>

<span data-ttu-id="f81c7-130">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f81c7-130">ALIASES</span></span>

## <span data-ttu-id="f81c7-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f81c7-131">RELATED LINKS</span></span>

