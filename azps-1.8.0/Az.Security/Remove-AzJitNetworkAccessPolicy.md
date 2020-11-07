---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b0414b6fbbd4cdb0211b7dee1f85e172c1329c3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659444"
---
# <span data-ttu-id="6fed1-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6fed1-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="6fed1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6fed1-102">SYNOPSIS</span></span>
<span data-ttu-id="6fed1-103">Löscht eine JIT-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="6fed1-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="6fed1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fed1-104">SYNTAX</span></span>

### <span data-ttu-id="6fed1-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="6fed1-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fed1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fed1-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fed1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6fed1-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fed1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fed1-108">DESCRIPTION</span></span>
<span data-ttu-id="6fed1-109">Löscht eine Just-in-Time-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="6fed1-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="6fed1-110">Nach dieser Aktion kann ein Benutzer keine temporäre Netzwerkverbindung auf den VMS anfordern, die innerhalb der gelöschten Richtlinie konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="6fed1-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="6fed1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6fed1-111">EXAMPLES</span></span>

### <span data-ttu-id="6fed1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6fed1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="6fed1-113">Löscht eine Just-in-Time-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="6fed1-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="6fed1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fed1-114">PARAMETERS</span></span>

### <span data-ttu-id="6fed1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fed1-115">-DefaultProfile</span></span>
<span data-ttu-id="6fed1-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6fed1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fed1-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6fed1-117">-InputObject</span></span>
<span data-ttu-id="6fed1-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="6fed1-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fed1-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="6fed1-119">-Location</span></span>
<span data-ttu-id="6fed1-120">Lage.</span><span class="sxs-lookup"><span data-stu-id="6fed1-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fed1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6fed1-121">-Name</span></span>
<span data-ttu-id="6fed1-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="6fed1-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fed1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fed1-123">-PassThru</span></span>
<span data-ttu-id="6fed1-124">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="6fed1-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="6fed1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fed1-125">-ResourceGroupName</span></span>
<span data-ttu-id="6fed1-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6fed1-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fed1-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6fed1-127">-ResourceId</span></span>
<span data-ttu-id="6fed1-128">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6fed1-128">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fed1-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6fed1-129">-Confirm</span></span>
<span data-ttu-id="6fed1-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fed1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fed1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fed1-131">-WhatIf</span></span>
<span data-ttu-id="6fed1-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fed1-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fed1-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fed1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fed1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fed1-134">CommonParameters</span></span>
<span data-ttu-id="6fed1-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fed1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fed1-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fed1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fed1-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6fed1-137">INPUTS</span></span>

### <span data-ttu-id="6fed1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6fed1-138">System.String</span></span>

### <span data-ttu-id="6fed1-139">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6fed1-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="6fed1-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6fed1-140">OUTPUTS</span></span>

### <span data-ttu-id="6fed1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6fed1-141">System.Boolean</span></span>

## <span data-ttu-id="6fed1-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="6fed1-142">NOTES</span></span>

## <span data-ttu-id="6fed1-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6fed1-143">RELATED LINKS</span></span>
