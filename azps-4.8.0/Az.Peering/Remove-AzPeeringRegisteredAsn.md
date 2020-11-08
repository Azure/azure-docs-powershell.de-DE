---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174924"
---
# <span data-ttu-id="b0b9b-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="b0b9b-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="b0b9b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b9b-103">Löschen oder entfernen Sie einen registrierten ASN aus der übergeordneten Peering-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b0b9b-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="b0b9b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0b9b-104">SYNTAX</span></span>

### <span data-ttu-id="b0b9b-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0b9b-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0b9b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b0b9b-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0b9b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0b9b-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0b9b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0b9b-108">DESCRIPTION</span></span>
<span data-ttu-id="b0b9b-109">Ermöglicht das Entfernen von registrierten ASN von übergeordneten Peering-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b0b9b-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="b0b9b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0b9b-110">EXAMPLES</span></span>

### <span data-ttu-id="b0b9b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b0b9b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="b0b9b-112">Entfernen einer registrierten ASN nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b0b9b-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="b0b9b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0b9b-113">PARAMETERS</span></span>

### <span data-ttu-id="b0b9b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0b9b-114">-AsJob</span></span>
<span data-ttu-id="b0b9b-115">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b0b9b-115">Run in the background.</span></span>

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

### <span data-ttu-id="b0b9b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b9b-116">-DefaultProfile</span></span>
<span data-ttu-id="b0b9b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0b9b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0b9b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b0b9b-118">-Force</span></span>
<span data-ttu-id="b0b9b-119">Erzwingen der Ausführung des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="b0b9b-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="b0b9b-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b0b9b-120">-InputObject</span></span>
<span data-ttu-id="b0b9b-121">Verwenden eines Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="b0b9b-121">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b9b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b0b9b-122">-Name</span></span>
<span data-ttu-id="b0b9b-123">Der Name der registrierten ASN-Datei</span><span class="sxs-lookup"><span data-stu-id="b0b9b-123">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b9b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0b9b-124">-PassThru</span></span>
<span data-ttu-id="b0b9b-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="b0b9b-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b0b9b-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="b0b9b-126">-PeeringName</span></span>
<span data-ttu-id="b0b9b-127">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b0b9b-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b9b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b9b-128">-ResourceGroupName</span></span>
<span data-ttu-id="b0b9b-129">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="b0b9b-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b9b-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b0b9b-130">-ResourceId</span></span>
<span data-ttu-id="b0b9b-131">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b0b9b-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b9b-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b0b9b-132">-Confirm</span></span>
<span data-ttu-id="b0b9b-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0b9b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0b9b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0b9b-134">-WhatIf</span></span>
<span data-ttu-id="b0b9b-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0b9b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0b9b-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0b9b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0b9b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b9b-137">CommonParameters</span></span>
<span data-ttu-id="b0b9b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b9b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b9b-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0b9b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b9b-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0b9b-140">INPUTS</span></span>

### <span data-ttu-id="b0b9b-141">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="b0b9b-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="b0b9b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b0b9b-142">System.String</span></span>

## <span data-ttu-id="b0b9b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0b9b-143">OUTPUTS</span></span>

### <span data-ttu-id="b0b9b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0b9b-144">System.Boolean</span></span>

## <span data-ttu-id="b0b9b-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0b9b-145">NOTES</span></span>

## <span data-ttu-id="b0b9b-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0b9b-146">RELATED LINKS</span></span>
