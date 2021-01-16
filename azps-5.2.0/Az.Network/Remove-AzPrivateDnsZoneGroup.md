---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291856"
---
# <span data-ttu-id="05729-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="05729-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="05729-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05729-102">SYNOPSIS</span></span>
<span data-ttu-id="05729-103">Entfernt eine DNS-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="05729-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="05729-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05729-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05729-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05729-105">DESCRIPTION</span></span>
<span data-ttu-id="05729-106">Das **Cmdlet "Remove-AzPrivateDnsZoneGroup"** entfernt eine DNS-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="05729-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="05729-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="05729-107">EXAMPLES</span></span>

### <span data-ttu-id="05729-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05729-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="05729-109">Im vorstehenden Beispiel wird eine DNS-Zonen-Grup namens "dnsgroup1" vom Endpunkt "test-pr-endpoint" entfernt.</span><span class="sxs-lookup"><span data-stu-id="05729-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="05729-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05729-110">PARAMETERS</span></span>

### <span data-ttu-id="05729-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05729-111">-AsJob</span></span>
<span data-ttu-id="05729-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="05729-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05729-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05729-113">-DefaultProfile</span></span>
<span data-ttu-id="05729-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05729-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05729-115">-Force</span><span class="sxs-lookup"><span data-stu-id="05729-115">-Force</span></span>
<span data-ttu-id="05729-116">Bestätigen Sie nicht, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="05729-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="05729-117">-Name</span><span class="sxs-lookup"><span data-stu-id="05729-117">-Name</span></span>
<span data-ttu-id="05729-118">Der Name der privaten Dns-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="05729-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05729-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05729-119">-PassThru</span></span>
<span data-ttu-id="05729-120">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="05729-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="05729-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="05729-121">-PrivateEndpointName</span></span>
<span data-ttu-id="05729-122">Der Name des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="05729-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="05729-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05729-123">-ResourceGroupName</span></span>
<span data-ttu-id="05729-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="05729-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="05729-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05729-125">-Confirm</span></span>
<span data-ttu-id="05729-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05729-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05729-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="05729-127">-WhatIf</span></span>
<span data-ttu-id="05729-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05729-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05729-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05729-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05729-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05729-130">CommonParameters</span></span>
<span data-ttu-id="05729-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05729-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05729-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05729-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05729-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="05729-133">INPUTS</span></span>

### <span data-ttu-id="05729-134">System.String</span><span class="sxs-lookup"><span data-stu-id="05729-134">System.String</span></span>

## <span data-ttu-id="05729-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="05729-135">OUTPUTS</span></span>

### <span data-ttu-id="05729-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="05729-136">System.Boolean</span></span>

## <span data-ttu-id="05729-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="05729-137">NOTES</span></span>

## <span data-ttu-id="05729-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="05729-138">RELATED LINKS</span></span>
