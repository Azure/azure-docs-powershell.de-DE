---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
ms.openlocfilehash: d314deb2515907b7d2b668d18d165a7fb0691509
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371256"
---
# <span data-ttu-id="58e9d-101">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="58e9d-101">New-AzServiceBusAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="58e9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="58e9d-103">Generiert eine SAS-Tolen für Azure Servicebus-Autorisierungsregel für Namespace/Warteschlange/Thema.</span><span class="sxs-lookup"><span data-stu-id="58e9d-103">Generates a SAS tolen for Azure servicebus authorization rule of namespace/queue/topic.</span></span> 

## <span data-ttu-id="58e9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58e9d-104">SYNTAX</span></span>

```
New-AzServiceBusAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58e9d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58e9d-105">DESCRIPTION</span></span>
<span data-ttu-id="58e9d-106">Das New-AzServiceBusAuthorizationRuleSASToken generiert ein SAS (Shared Access Signature)-Token für azure Eventhub Namesapce oder Azure Eventhub.</span><span class="sxs-lookup"><span data-stu-id="58e9d-106">The New-AzServiceBusAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="58e9d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58e9d-107">EXAMPLES</span></span>

### <span data-ttu-id="58e9d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58e9d-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="58e9d-109">Generieren Sie das SAS-Token für die angegebene Erstellungsregel für den Namespace mit Start- und Ablaufzeit.</span><span class="sxs-lookup"><span data-stu-id="58e9d-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="58e9d-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="58e9d-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="58e9d-111">Generieren Sie das SAS-Token für die angegebene Erstellungsregel für den Namespace mit Ablaufzeit.</span><span class="sxs-lookup"><span data-stu-id="58e9d-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="58e9d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58e9d-112">PARAMETERS</span></span>

### <span data-ttu-id="58e9d-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="58e9d-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="58e9d-114">ARM ResourceId der Authoraization Rule</span><span class="sxs-lookup"><span data-stu-id="58e9d-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="58e9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e9d-115">-DefaultProfile</span></span>
<span data-ttu-id="58e9d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58e9d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58e9d-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="58e9d-117">-ExpiryTime</span></span>
<span data-ttu-id="58e9d-118">Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="58e9d-118">Expiry Time</span></span>

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

### <span data-ttu-id="58e9d-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="58e9d-119">-KeyType</span></span>
<span data-ttu-id="58e9d-120">Schlüsseltyp</span><span class="sxs-lookup"><span data-stu-id="58e9d-120">Key Type</span></span>

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

### <span data-ttu-id="58e9d-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="58e9d-121">-StartTime</span></span>
<span data-ttu-id="58e9d-122">Startzeit</span><span class="sxs-lookup"><span data-stu-id="58e9d-122">Start Time</span></span>

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

### <span data-ttu-id="58e9d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58e9d-123">-Confirm</span></span>
<span data-ttu-id="58e9d-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58e9d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58e9d-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="58e9d-125">-WhatIf</span></span>
<span data-ttu-id="58e9d-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58e9d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58e9d-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58e9d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58e9d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e9d-128">CommonParameters</span></span>
<span data-ttu-id="58e9d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e9d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="58e9d-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58e9d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e9d-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58e9d-131">INPUTS</span></span>

### <span data-ttu-id="58e9d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="58e9d-132">System.String</span></span>

### <span data-ttu-id="58e9d-133">System.Nullable'1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="58e9d-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="58e9d-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58e9d-134">OUTPUTS</span></span>

### <span data-ttu-id="58e9d-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="58e9d-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="58e9d-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="58e9d-136">NOTES</span></span>

## <span data-ttu-id="58e9d-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="58e9d-137">RELATED LINKS</span></span>