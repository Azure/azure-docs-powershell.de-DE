---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
ms.openlocfilehash: dd7b387631d399027cbf3dd3e27db5a3cb5ae8bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824792"
---
# <span data-ttu-id="83e3f-101">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="83e3f-101">New-AzServiceBusAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="83e3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="83e3f-103">Generiert eine SAS-tolen für Azure ServiceBus-Autorisierungsregel für Namespace/Queue/Topic.</span><span class="sxs-lookup"><span data-stu-id="83e3f-103">Generates a SAS tolen for Azure servicebus authorization rule of namespace/queue/topic.</span></span> 

## <span data-ttu-id="83e3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83e3f-104">SYNTAX</span></span>

```
New-AzServiceBusAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83e3f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83e3f-105">DESCRIPTION</span></span>
<span data-ttu-id="83e3f-106">Das New-AzServiceBusAuthorizationRuleSASToken-Cmdlet generiert ein SAS-Token (Shared Access Signature) für ein Azure Eventhub Namespace oder Azure Eventhub</span><span class="sxs-lookup"><span data-stu-id="83e3f-106">The New-AzServiceBusAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="83e3f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83e3f-107">EXAMPLES</span></span>

### <span data-ttu-id="83e3f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="83e3f-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="83e3f-109">Generiert ein SAS-Token für die angegebene authorixation-Regel für Namespace mit Start-und Ablaufzeit.</span><span class="sxs-lookup"><span data-stu-id="83e3f-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="83e3f-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="83e3f-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="83e3f-111">Generiert ein SAS-Token für die angegebene authorixation-Regel für Namespace mit Ablaufzeit.</span><span class="sxs-lookup"><span data-stu-id="83e3f-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="83e3f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="83e3f-112">PARAMETERS</span></span>

### <span data-ttu-id="83e3f-113">-AuthorizationRule-Nr</span><span class="sxs-lookup"><span data-stu-id="83e3f-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="83e3f-114">Arm-Authoraization-Regel</span><span class="sxs-lookup"><span data-stu-id="83e3f-114">ARM ResourceId of the Authoraization Rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83e3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e3f-115">-DefaultProfile</span></span>
<span data-ttu-id="83e3f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83e3f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83e3f-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="83e3f-117">-ExpiryTime</span></span>
<span data-ttu-id="83e3f-118">Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="83e3f-118">Expiry Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83e3f-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="83e3f-119">-KeyType</span></span>
<span data-ttu-id="83e3f-120">Schlüsseltyp</span><span class="sxs-lookup"><span data-stu-id="83e3f-120">Key Type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83e3f-121">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="83e3f-121">-StartTime</span></span>
<span data-ttu-id="83e3f-122">Startzeit</span><span class="sxs-lookup"><span data-stu-id="83e3f-122">Start Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83e3f-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83e3f-123">-Confirm</span></span>
<span data-ttu-id="83e3f-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83e3f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83e3f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83e3f-125">-WhatIf</span></span>
<span data-ttu-id="83e3f-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83e3f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83e3f-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83e3f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83e3f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e3f-128">CommonParameters</span></span>
<span data-ttu-id="83e3f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83e3f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="83e3f-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83e3f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e3f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83e3f-131">INPUTS</span></span>

### <span data-ttu-id="83e3f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="83e3f-132">System.String</span></span>

### <span data-ttu-id="83e3f-133">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="83e3f-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="83e3f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83e3f-134">OUTPUTS</span></span>

### <span data-ttu-id="83e3f-135">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="83e3f-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="83e3f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="83e3f-136">NOTES</span></span>

## <span data-ttu-id="83e3f-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83e3f-137">RELATED LINKS</span></span>