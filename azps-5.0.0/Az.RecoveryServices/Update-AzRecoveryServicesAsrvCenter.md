---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179374"
---
# <span data-ttu-id="4b820-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="4b820-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="4b820-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b820-102">SYNOPSIS</span></span>
<span data-ttu-id="4b820-103">Aktualisieren Sie die Ermittlungs Details für ein registriertes vCenter.</span><span class="sxs-lookup"><span data-stu-id="4b820-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="4b820-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b820-104">SYNTAX</span></span>

### <span data-ttu-id="4b820-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b820-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b820-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b820-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b820-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b820-107">DESCRIPTION</span></span>
<span data-ttu-id="4b820-108">Das Cmdlet **Update-AzRecoveryServicesAsrvCenter** ist eine Aktualisierungs Ermittlungs Details für ein registriertes vCenter.</span><span class="sxs-lookup"><span data-stu-id="4b820-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="4b820-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b820-109">EXAMPLES</span></span>

### <span data-ttu-id="4b820-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b820-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="4b820-111">Aktualisieren Sie die Ermittlungs Details für ein registriertes vCenter.</span><span class="sxs-lookup"><span data-stu-id="4b820-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="4b820-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b820-112">PARAMETERS</span></span>

### <span data-ttu-id="4b820-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="4b820-113">-Account</span></span>
<span data-ttu-id="4b820-114">vCenter-Anmeldeinformationen-Konto.</span><span class="sxs-lookup"><span data-stu-id="4b820-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b820-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b820-115">-DefaultProfile</span></span>
<span data-ttu-id="4b820-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b820-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b820-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4b820-117">-InputObject</span></span>
<span data-ttu-id="4b820-118">Das vCenter Server-Objekt, für das die Ermittlungs Details aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4b820-118">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b820-119">-Port</span><span class="sxs-lookup"><span data-stu-id="4b820-119">-Port</span></span>
<span data-ttu-id="4b820-120">Der TCP-Port auf dem vCenter Server, der für die Erkennung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b820-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b820-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4b820-121">-ResourceId</span></span>
<span data-ttu-id="4b820-122">Gibt die Resourcen-Nr von vCenter an.</span><span class="sxs-lookup"><span data-stu-id="4b820-122">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b820-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b820-123">-Confirm</span></span>
<span data-ttu-id="4b820-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b820-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b820-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b820-125">-WhatIf</span></span>
<span data-ttu-id="4b820-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b820-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b820-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b820-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b820-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b820-128">CommonParameters</span></span>
<span data-ttu-id="4b820-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b820-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b820-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b820-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b820-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b820-131">INPUTS</span></span>

### <span data-ttu-id="4b820-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4b820-132">System.String</span></span>

### <span data-ttu-id="4b820-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="4b820-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="4b820-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b820-134">OUTPUTS</span></span>

### <span data-ttu-id="4b820-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4b820-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4b820-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b820-136">NOTES</span></span>

## <span data-ttu-id="4b820-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b820-137">RELATED LINKS</span></span>
