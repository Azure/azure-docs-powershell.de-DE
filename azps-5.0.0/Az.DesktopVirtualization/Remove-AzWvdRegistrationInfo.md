---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296992"
---
# <span data-ttu-id="56500-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="56500-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="56500-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56500-102">SYNOPSIS</span></span>
<span data-ttu-id="56500-103">Entfernen Sie die Registrierungsinformationen für Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="56500-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="56500-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56500-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56500-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56500-105">DESCRIPTION</span></span>
<span data-ttu-id="56500-106">Entfernen Sie die Registrierungsinformationen für Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="56500-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="56500-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56500-107">EXAMPLES</span></span>

### <span data-ttu-id="56500-108">Beispiel 1: Löschen eines Windows Virtual Desktop-Registrierungs Tokens</span><span class="sxs-lookup"><span data-stu-id="56500-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="56500-109">Mit diesem Befehl wird ein Windows Virtual Desktop-Registrierungs Token in einem Host Pool gelöscht.</span><span class="sxs-lookup"><span data-stu-id="56500-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="56500-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="56500-110">PARAMETERS</span></span>

### <span data-ttu-id="56500-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56500-111">-DefaultProfile</span></span>
<span data-ttu-id="56500-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56500-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56500-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="56500-113">-HostPoolName</span></span>
<span data-ttu-id="56500-114">Name des Host Pools</span><span class="sxs-lookup"><span data-stu-id="56500-114">Host Pool Name</span></span>

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

### <span data-ttu-id="56500-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56500-115">-ResourceGroupName</span></span>
<span data-ttu-id="56500-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="56500-116">Resource Group Name</span></span>

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

### <span data-ttu-id="56500-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="56500-117">-SubscriptionId</span></span>
<span data-ttu-id="56500-118">Hilfe foo 1</span><span class="sxs-lookup"><span data-stu-id="56500-118">help foo 1</span></span>

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

### <span data-ttu-id="56500-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="56500-119">-Confirm</span></span>
<span data-ttu-id="56500-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56500-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56500-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56500-121">-WhatIf</span></span>
<span data-ttu-id="56500-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56500-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56500-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56500-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56500-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56500-124">CommonParameters</span></span>
<span data-ttu-id="56500-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56500-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56500-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56500-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56500-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56500-127">INPUTS</span></span>

## <span data-ttu-id="56500-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56500-128">OUTPUTS</span></span>

## <span data-ttu-id="56500-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="56500-129">NOTES</span></span>

<span data-ttu-id="56500-130">Aliase</span><span class="sxs-lookup"><span data-stu-id="56500-130">ALIASES</span></span>

## <span data-ttu-id="56500-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56500-131">RELATED LINKS</span></span>

