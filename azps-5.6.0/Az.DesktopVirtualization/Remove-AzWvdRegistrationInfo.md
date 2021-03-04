---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: 548e7d19e2d5285ed4063bc9c14202980c02028d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932880"
---
# <span data-ttu-id="4bdc5-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="4bdc5-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="4bdc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bdc5-102">SYNOPSIS</span></span>
<span data-ttu-id="4bdc5-103">Entfernen Sie die Registrierungsinformationen für den virtuellen Windows-Desktop.</span><span class="sxs-lookup"><span data-stu-id="4bdc5-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="4bdc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bdc5-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4bdc5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bdc5-105">DESCRIPTION</span></span>
<span data-ttu-id="4bdc5-106">Entfernen Sie die Registrierungsinformationen für den virtuellen Windows-Desktop.</span><span class="sxs-lookup"><span data-stu-id="4bdc5-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="4bdc5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4bdc5-107">EXAMPLES</span></span>

### <span data-ttu-id="4bdc5-108">Beispiel 1: Löschen eines Virtuellen Windows-Desktopregistrierungstokens</span><span class="sxs-lookup"><span data-stu-id="4bdc5-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="4bdc5-109">Mit diesem Befehl wird ein Windows Virtual Desktop Registration Token in einem Hostpool gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4bdc5-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="4bdc5-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4bdc5-110">PARAMETERS</span></span>

### <span data-ttu-id="4bdc5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bdc5-111">-DefaultProfile</span></span>
<span data-ttu-id="4bdc5-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bdc5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bdc5-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="4bdc5-113">-HostPoolName</span></span>
<span data-ttu-id="4bdc5-114">Name des Hostpools</span><span class="sxs-lookup"><span data-stu-id="4bdc5-114">Host Pool Name</span></span>

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

### <span data-ttu-id="4bdc5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bdc5-115">-ResourceGroupName</span></span>
<span data-ttu-id="4bdc5-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="4bdc5-116">Resource Group Name</span></span>

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

### <span data-ttu-id="4bdc5-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4bdc5-117">-SubscriptionId</span></span>
<span data-ttu-id="4bdc5-118">Hilfe foo 1</span><span class="sxs-lookup"><span data-stu-id="4bdc5-118">help foo 1</span></span>

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

### <span data-ttu-id="4bdc5-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4bdc5-119">-Confirm</span></span>
<span data-ttu-id="4bdc5-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4bdc5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bdc5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bdc5-121">-WhatIf</span></span>
<span data-ttu-id="4bdc5-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4bdc5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bdc5-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bdc5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bdc5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bdc5-124">CommonParameters</span></span>
<span data-ttu-id="4bdc5-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bdc5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bdc5-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bdc5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bdc5-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4bdc5-127">INPUTS</span></span>

## <span data-ttu-id="4bdc5-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4bdc5-128">OUTPUTS</span></span>

## <span data-ttu-id="4bdc5-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4bdc5-129">NOTES</span></span>

<span data-ttu-id="4bdc5-130">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4bdc5-130">ALIASES</span></span>

## <span data-ttu-id="4bdc5-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4bdc5-131">RELATED LINKS</span></span>

