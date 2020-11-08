---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178449"
---
# <span data-ttu-id="936dd-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="936dd-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="936dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="936dd-102">SYNOPSIS</span></span>
<span data-ttu-id="936dd-103">Entfernt einen privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="936dd-103">Removes a private link service</span></span>

## <span data-ttu-id="936dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="936dd-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="936dd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="936dd-105">DESCRIPTION</span></span>
<span data-ttu-id="936dd-106">Das Cmdlet " **Remove-AzPrivateLinkService** " entfernt einen privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="936dd-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="936dd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="936dd-107">EXAMPLES</span></span>

### <span data-ttu-id="936dd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="936dd-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="936dd-109">In diesem Beispiel wird ein privater Link Dienst mit dem Namen TestPrivateLinkService entfernt.</span><span class="sxs-lookup"><span data-stu-id="936dd-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="936dd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="936dd-110">PARAMETERS</span></span>

### <span data-ttu-id="936dd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="936dd-111">-AsJob</span></span>
<span data-ttu-id="936dd-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="936dd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="936dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="936dd-113">-DefaultProfile</span></span>
<span data-ttu-id="936dd-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="936dd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="936dd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="936dd-115">-Force</span></span>
<span data-ttu-id="936dd-116">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="936dd-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="936dd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="936dd-117">-Name</span></span>
<span data-ttu-id="936dd-118">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="936dd-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936dd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="936dd-119">-PassThru</span></span>
<span data-ttu-id="936dd-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="936dd-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="936dd-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="936dd-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="936dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="936dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="936dd-123">Der Ressourcengruppenname des privaten Link Diensts.</span><span class="sxs-lookup"><span data-stu-id="936dd-123">The resource group name of the private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936dd-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="936dd-124">-Confirm</span></span>
<span data-ttu-id="936dd-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="936dd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="936dd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="936dd-126">-WhatIf</span></span>
<span data-ttu-id="936dd-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="936dd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="936dd-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="936dd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="936dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="936dd-129">CommonParameters</span></span>
<span data-ttu-id="936dd-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="936dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="936dd-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="936dd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="936dd-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="936dd-132">INPUTS</span></span>

### <span data-ttu-id="936dd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="936dd-133">System.String</span></span>

## <span data-ttu-id="936dd-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="936dd-134">OUTPUTS</span></span>

### <span data-ttu-id="936dd-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="936dd-135">System.Boolean</span></span>

## <span data-ttu-id="936dd-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="936dd-136">NOTES</span></span>

## <span data-ttu-id="936dd-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="936dd-137">RELATED LINKS</span></span>

[<span data-ttu-id="936dd-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="936dd-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="936dd-139">Neu – AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="936dd-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)