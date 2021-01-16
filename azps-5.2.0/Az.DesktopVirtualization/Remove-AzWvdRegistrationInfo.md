---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296969"
---
# <span data-ttu-id="ed524-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="ed524-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="ed524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed524-102">SYNOPSIS</span></span>
<span data-ttu-id="ed524-103">Entfernen Sie die Registrierungsinformationen für den virtuellen Windows-Desktop.</span><span class="sxs-lookup"><span data-stu-id="ed524-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="ed524-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed524-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed524-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed524-105">DESCRIPTION</span></span>
<span data-ttu-id="ed524-106">Entfernen Sie die Registrierungsinformationen für den virtuellen Windows-Desktop.</span><span class="sxs-lookup"><span data-stu-id="ed524-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="ed524-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed524-107">EXAMPLES</span></span>

### <span data-ttu-id="ed524-108">Beispiel 1: Löschen eines Tokens für die Registrierung des virtuellen Windows-Desktops</span><span class="sxs-lookup"><span data-stu-id="ed524-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="ed524-109">Mit diesem Befehl wird ein Windows Virtual Desktop Registration Token in einem Hostpool gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ed524-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="ed524-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed524-110">PARAMETERS</span></span>

### <span data-ttu-id="ed524-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed524-111">-DefaultProfile</span></span>
<span data-ttu-id="ed524-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed524-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed524-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ed524-113">-HostPoolName</span></span>
<span data-ttu-id="ed524-114">Name des Hostpools</span><span class="sxs-lookup"><span data-stu-id="ed524-114">Host Pool Name</span></span>

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

### <span data-ttu-id="ed524-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed524-115">-ResourceGroupName</span></span>
<span data-ttu-id="ed524-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ed524-116">Resource Group Name</span></span>

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

### <span data-ttu-id="ed524-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed524-117">-SubscriptionId</span></span>
<span data-ttu-id="ed524-118">Hilfe foo 1</span><span class="sxs-lookup"><span data-stu-id="ed524-118">help foo 1</span></span>

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

### <span data-ttu-id="ed524-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed524-119">-Confirm</span></span>
<span data-ttu-id="ed524-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed524-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed524-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ed524-121">-WhatIf</span></span>
<span data-ttu-id="ed524-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed524-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed524-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed524-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed524-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed524-124">CommonParameters</span></span>
<span data-ttu-id="ed524-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed524-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed524-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed524-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed524-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed524-127">INPUTS</span></span>

## <span data-ttu-id="ed524-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed524-128">OUTPUTS</span></span>

## <span data-ttu-id="ed524-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ed524-129">NOTES</span></span>

<span data-ttu-id="ed524-130">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ed524-130">ALIASES</span></span>

## <span data-ttu-id="ed524-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ed524-131">RELATED LINKS</span></span>

