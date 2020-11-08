---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165144"
---
# <span data-ttu-id="dece8-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="dece8-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="dece8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dece8-102">SYNOPSIS</span></span>
<span data-ttu-id="dece8-103">Entfernt eine DNS-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="dece8-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="dece8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dece8-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dece8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dece8-105">DESCRIPTION</span></span>
<span data-ttu-id="dece8-106">Das Cmdlet **Remove-AzPrivateDnsZoneGroup** entfernt eine DNS-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="dece8-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="dece8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dece8-107">EXAMPLES</span></span>

### <span data-ttu-id="dece8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dece8-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="dece8-109">Im obigen Beispiel wird eine DNS-Zone Grup mit dem Namen dnsgroup1 vom Endpunkt Test-PR-Endpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="dece8-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="dece8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dece8-110">PARAMETERS</span></span>

### <span data-ttu-id="dece8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dece8-111">-AsJob</span></span>
<span data-ttu-id="dece8-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dece8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dece8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dece8-113">-DefaultProfile</span></span>
<span data-ttu-id="dece8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dece8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dece8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dece8-115">-Force</span></span>
<span data-ttu-id="dece8-116">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="dece8-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="dece8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dece8-117">-Name</span></span>
<span data-ttu-id="dece8-118">Der Name der privaten DNS-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="dece8-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="dece8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dece8-119">-PassThru</span></span>
<span data-ttu-id="dece8-120">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="dece8-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="dece8-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="dece8-121">-PrivateEndpointName</span></span>
<span data-ttu-id="dece8-122">Der Name des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="dece8-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="dece8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dece8-123">-ResourceGroupName</span></span>
<span data-ttu-id="dece8-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dece8-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="dece8-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dece8-125">-Confirm</span></span>
<span data-ttu-id="dece8-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dece8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dece8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dece8-127">-WhatIf</span></span>
<span data-ttu-id="dece8-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dece8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dece8-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dece8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dece8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dece8-130">CommonParameters</span></span>
<span data-ttu-id="dece8-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dece8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dece8-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dece8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dece8-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dece8-133">INPUTS</span></span>

### <span data-ttu-id="dece8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dece8-134">System.String</span></span>

## <span data-ttu-id="dece8-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dece8-135">OUTPUTS</span></span>

### <span data-ttu-id="dece8-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dece8-136">System.Boolean</span></span>

## <span data-ttu-id="dece8-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="dece8-137">NOTES</span></span>

## <span data-ttu-id="dece8-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dece8-138">RELATED LINKS</span></span>
