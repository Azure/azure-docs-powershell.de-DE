---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 24348c44ef9b529507c50a689f181739d1474e22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173801"
---
# <span data-ttu-id="74ed9-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="74ed9-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="74ed9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="74ed9-103">Generiert ein SAS-Token für Azure eventhub-Autorisierungsregel für Namespace-eventhub.</span><span class="sxs-lookup"><span data-stu-id="74ed9-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="74ed9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74ed9-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74ed9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74ed9-105">DESCRIPTION</span></span>
<span data-ttu-id="74ed9-106">Das New-AzEventHubAuthorizationRuleSASToken-Cmdlet generiert ein SAS-Token (Shared Access Signature) für ein Azure Eventhub Namespace oder Azure Eventhub</span><span class="sxs-lookup"><span data-stu-id="74ed9-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="74ed9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74ed9-107">EXAMPLES</span></span>

### <span data-ttu-id="74ed9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74ed9-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="74ed9-109">Generiert ein SAS-Token für die angegebene authorixation-Regel für Namespace mit Start-und Ablaufzeit.</span><span class="sxs-lookup"><span data-stu-id="74ed9-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="74ed9-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="74ed9-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="74ed9-111">Generiert ein SAS-Token für die angegebene authorixation-Regel für Namespace mit Ablaufzeit.</span><span class="sxs-lookup"><span data-stu-id="74ed9-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="74ed9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="74ed9-112">PARAMETERS</span></span>

### <span data-ttu-id="74ed9-113">-AuthorizationRule-Nr</span><span class="sxs-lookup"><span data-stu-id="74ed9-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="74ed9-114">Arm-Authoraization-Regel</span><span class="sxs-lookup"><span data-stu-id="74ed9-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="74ed9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ed9-115">-DefaultProfile</span></span>
<span data-ttu-id="74ed9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74ed9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74ed9-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="74ed9-117">-ExpiryTime</span></span>
<span data-ttu-id="74ed9-118">Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="74ed9-118">Expiry Time</span></span>

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

### <span data-ttu-id="74ed9-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="74ed9-119">-KeyType</span></span>
<span data-ttu-id="74ed9-120">Schlüsseltyp</span><span class="sxs-lookup"><span data-stu-id="74ed9-120">Key Type</span></span>

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

### <span data-ttu-id="74ed9-121">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="74ed9-121">-StartTime</span></span>
<span data-ttu-id="74ed9-122">Startzeit</span><span class="sxs-lookup"><span data-stu-id="74ed9-122">Start Time</span></span>

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

### <span data-ttu-id="74ed9-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74ed9-123">-Confirm</span></span>
<span data-ttu-id="74ed9-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74ed9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74ed9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74ed9-125">-WhatIf</span></span>
<span data-ttu-id="74ed9-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74ed9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74ed9-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74ed9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74ed9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ed9-128">CommonParameters</span></span>
<span data-ttu-id="74ed9-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74ed9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="74ed9-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74ed9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ed9-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74ed9-131">INPUTS</span></span>

### <span data-ttu-id="74ed9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="74ed9-132">System.String</span></span>

### <span data-ttu-id="74ed9-133">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="74ed9-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="74ed9-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74ed9-134">OUTPUTS</span></span>

### <span data-ttu-id="74ed9-135">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="74ed9-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="74ed9-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="74ed9-136">NOTES</span></span>

## <span data-ttu-id="74ed9-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74ed9-137">RELATED LINKS</span></span>
