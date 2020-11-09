---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301821"
---
# <span data-ttu-id="cedc0-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cedc0-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="cedc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cedc0-102">SYNOPSIS</span></span>
<span data-ttu-id="cedc0-103">Löscht eine Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="cedc0-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="cedc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cedc0-104">SYNTAX</span></span>

### <span data-ttu-id="cedc0-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cedc0-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cedc0-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cedc0-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cedc0-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cedc0-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cedc0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cedc0-108">DESCRIPTION</span></span>
<span data-ttu-id="cedc0-109">Das Cmdlet **Remove-AzSecurityPartnerProvider** löscht eine Azure-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cedc0-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="cedc0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cedc0-110">EXAMPLES</span></span>

### <span data-ttu-id="cedc0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cedc0-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="cedc0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cedc0-112">PARAMETERS</span></span>

### <span data-ttu-id="cedc0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cedc0-113">-AsJob</span></span>
<span data-ttu-id="cedc0-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cedc0-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedc0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cedc0-115">-DefaultProfile</span></span>
<span data-ttu-id="cedc0-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cedc0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedc0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cedc0-117">-Force</span></span>
<span data-ttu-id="cedc0-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="cedc0-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedc0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cedc0-119">-Name</span></span>
<span data-ttu-id="cedc0-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="cedc0-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cedc0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cedc0-121">-PassThru</span></span>
<span data-ttu-id="cedc0-122">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cedc0-122">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedc0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cedc0-123">-ResourceGroupName</span></span>
<span data-ttu-id="cedc0-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cedc0-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cedc0-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cedc0-125">-ResourceId</span></span>
<span data-ttu-id="cedc0-126">Die securityPartnerProvider-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="cedc0-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cedc0-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cedc0-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="cedc0-128">Das securityPartnerProvider-Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="cedc0-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cedc0-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cedc0-129">-Confirm</span></span>
<span data-ttu-id="cedc0-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cedc0-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedc0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cedc0-131">-WhatIf</span></span>
<span data-ttu-id="cedc0-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cedc0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cedc0-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cedc0-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedc0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cedc0-134">CommonParameters</span></span>
<span data-ttu-id="cedc0-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cedc0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cedc0-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cedc0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cedc0-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cedc0-137">INPUTS</span></span>

### <span data-ttu-id="cedc0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cedc0-138">System.String</span></span>

### <span data-ttu-id="cedc0-139">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cedc0-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="cedc0-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cedc0-140">OUTPUTS</span></span>

### <span data-ttu-id="cedc0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cedc0-141">System.Boolean</span></span>

## <span data-ttu-id="cedc0-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="cedc0-142">NOTES</span></span>

## <span data-ttu-id="cedc0-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cedc0-143">RELATED LINKS</span></span>
