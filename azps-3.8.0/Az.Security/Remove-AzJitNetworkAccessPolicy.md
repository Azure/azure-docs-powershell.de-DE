---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 21a31d2d4e094e986ad862bfe69baef98148e5f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996289"
---
# <span data-ttu-id="cfcdd-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cfcdd-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="cfcdd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cfcdd-102">SYNOPSIS</span></span>
<span data-ttu-id="cfcdd-103">Löscht eine JIT-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="cfcdd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfcdd-104">SYNTAX</span></span>

### <span data-ttu-id="cfcdd-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="cfcdd-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfcdd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfcdd-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfcdd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="cfcdd-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfcdd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cfcdd-108">DESCRIPTION</span></span>
<span data-ttu-id="cfcdd-109">Löscht eine Just-in-Time-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="cfcdd-110">Nach dieser Aktion kann ein Benutzer keine temporäre Netzwerkverbindung auf den VMS anfordern, die innerhalb der gelöschten Richtlinie konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="cfcdd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cfcdd-111">EXAMPLES</span></span>

### <span data-ttu-id="cfcdd-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cfcdd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="cfcdd-113">Löscht eine Just-in-Time-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="cfcdd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfcdd-114">PARAMETERS</span></span>

### <span data-ttu-id="cfcdd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfcdd-115">-DefaultProfile</span></span>
<span data-ttu-id="cfcdd-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfcdd-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cfcdd-117">-InputObject</span></span>
<span data-ttu-id="cfcdd-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-118">Input Object.</span></span>

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

### <span data-ttu-id="cfcdd-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="cfcdd-119">-Location</span></span>
<span data-ttu-id="cfcdd-120">Lage.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-120">Location.</span></span>

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

### <span data-ttu-id="cfcdd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cfcdd-121">-Name</span></span>
<span data-ttu-id="cfcdd-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="cfcdd-122">Resource name.</span></span>

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

### <span data-ttu-id="cfcdd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfcdd-123">-PassThru</span></span>
<span data-ttu-id="cfcdd-124">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="cfcdd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfcdd-125">-ResourceGroupName</span></span>
<span data-ttu-id="cfcdd-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-126">Resource group name.</span></span>

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

### <span data-ttu-id="cfcdd-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cfcdd-127">-ResourceId</span></span>
<span data-ttu-id="cfcdd-128">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-128">Resource ID.</span></span>

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

### <span data-ttu-id="cfcdd-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cfcdd-129">-Confirm</span></span>
<span data-ttu-id="cfcdd-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfcdd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfcdd-131">-WhatIf</span></span>
<span data-ttu-id="cfcdd-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfcdd-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfcdd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfcdd-134">CommonParameters</span></span>
<span data-ttu-id="cfcdd-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfcdd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfcdd-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfcdd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfcdd-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cfcdd-137">INPUTS</span></span>

### <span data-ttu-id="cfcdd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cfcdd-138">System.String</span></span>

### <span data-ttu-id="cfcdd-139">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cfcdd-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="cfcdd-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cfcdd-140">OUTPUTS</span></span>

### <span data-ttu-id="cfcdd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cfcdd-141">System.Boolean</span></span>

## <span data-ttu-id="cfcdd-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="cfcdd-142">NOTES</span></span>

## <span data-ttu-id="cfcdd-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cfcdd-143">RELATED LINKS</span></span>
