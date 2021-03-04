---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 72b7fa033696fb5daba364a45713294a8b54831b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922760"
---
# <span data-ttu-id="fb33c-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb33c-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="fb33c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb33c-102">SYNOPSIS</span></span>
<span data-ttu-id="fb33c-103">Entfernt eine Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="fb33c-103">Removes an application security group.</span></span>

## <span data-ttu-id="fb33c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb33c-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb33c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb33c-105">DESCRIPTION</span></span>
<span data-ttu-id="fb33c-106">Das **Cmdlet Remove-AzApplicationSecurityGroup** entfernt eine Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="fb33c-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="fb33c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fb33c-107">EXAMPLES</span></span>

### <span data-ttu-id="fb33c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fb33c-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="fb33c-109">Mit diesem Befehl wird eine Anwendungssicherheitsgruppe mit dem Namen MyApplicationSecurityGrouo in der Ressourcengruppe "MyResourceGroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fb33c-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="fb33c-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fb33c-110">PARAMETERS</span></span>

### <span data-ttu-id="fb33c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb33c-111">-AsJob</span></span>
<span data-ttu-id="fb33c-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fb33c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb33c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb33c-113">-DefaultProfile</span></span>
<span data-ttu-id="fb33c-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb33c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb33c-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="fb33c-115">-Force</span></span>
<span data-ttu-id="fb33c-116">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="fb33c-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="fb33c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fb33c-117">-Name</span></span>
<span data-ttu-id="fb33c-118">Der Name der Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="fb33c-118">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb33c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb33c-119">-PassThru</span></span>
<span data-ttu-id="fb33c-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="fb33c-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="fb33c-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="fb33c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb33c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb33c-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb33c-123">Der Ressourcengruppenname der Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="fb33c-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="fb33c-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb33c-124">-Confirm</span></span>
<span data-ttu-id="fb33c-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb33c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb33c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb33c-126">-WhatIf</span></span>
<span data-ttu-id="fb33c-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb33c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb33c-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb33c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb33c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb33c-129">CommonParameters</span></span>
<span data-ttu-id="fb33c-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb33c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb33c-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb33c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb33c-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fb33c-132">INPUTS</span></span>

### <span data-ttu-id="fb33c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fb33c-133">System.String</span></span>

## <span data-ttu-id="fb33c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fb33c-134">OUTPUTS</span></span>

### <span data-ttu-id="fb33c-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb33c-135">System.Boolean</span></span>

## <span data-ttu-id="fb33c-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fb33c-136">NOTES</span></span>

## <span data-ttu-id="fb33c-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fb33c-137">RELATED LINKS</span></span>

[<span data-ttu-id="fb33c-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb33c-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="fb33c-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb33c-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
