---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166962"
---
# <span data-ttu-id="dfc2a-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="dfc2a-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="dfc2a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dfc2a-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc2a-103">Entfernen Sie die Registrierungsinformationen für Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="dfc2a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfc2a-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dfc2a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfc2a-105">DESCRIPTION</span></span>
<span data-ttu-id="dfc2a-106">Entfernen Sie die Registrierungsinformationen für Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="dfc2a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dfc2a-107">EXAMPLES</span></span>

### <span data-ttu-id="dfc2a-108">Beispiel 1: Löschen eines Windows Virtual Desktop-Registrierungs Tokens</span><span class="sxs-lookup"><span data-stu-id="dfc2a-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="dfc2a-109">Mit diesem Befehl wird ein Windows Virtual Desktop-Registrierungs Token in einem Host Pool gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="dfc2a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfc2a-110">PARAMETERS</span></span>

### <span data-ttu-id="dfc2a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc2a-111">-DefaultProfile</span></span>
<span data-ttu-id="dfc2a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfc2a-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="dfc2a-113">-HostPoolName</span></span>
<span data-ttu-id="dfc2a-114">Name des Host Pools</span><span class="sxs-lookup"><span data-stu-id="dfc2a-114">Host Pool Name</span></span>

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

### <span data-ttu-id="dfc2a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfc2a-115">-ResourceGroupName</span></span>
<span data-ttu-id="dfc2a-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="dfc2a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="dfc2a-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="dfc2a-117">-SubscriptionId</span></span>
<span data-ttu-id="dfc2a-118">Hilfe foo 1</span><span class="sxs-lookup"><span data-stu-id="dfc2a-118">help foo 1</span></span>

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

### <span data-ttu-id="dfc2a-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dfc2a-119">-Confirm</span></span>
<span data-ttu-id="dfc2a-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfc2a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfc2a-121">-WhatIf</span></span>
<span data-ttu-id="dfc2a-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfc2a-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfc2a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc2a-124">CommonParameters</span></span>
<span data-ttu-id="dfc2a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc2a-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfc2a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc2a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dfc2a-127">INPUTS</span></span>

## <span data-ttu-id="dfc2a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dfc2a-128">OUTPUTS</span></span>

## <span data-ttu-id="dfc2a-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="dfc2a-129">NOTES</span></span>

<span data-ttu-id="dfc2a-130">Aliase</span><span class="sxs-lookup"><span data-stu-id="dfc2a-130">ALIASES</span></span>

## <span data-ttu-id="dfc2a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dfc2a-131">RELATED LINKS</span></span>

