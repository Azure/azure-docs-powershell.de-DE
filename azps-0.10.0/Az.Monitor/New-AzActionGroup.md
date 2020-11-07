---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 9d29240e4be9039e75491ede7d835ecba99aa2d5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842012"
---
# <span data-ttu-id="8ed2c-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="8ed2c-101">New-AzActionGroup</span></span>

## <span data-ttu-id="8ed2c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ed2c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed2c-103">Erstellt ein Aktions Gruppenverweis-Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="8ed2c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ed2c-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ed2c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ed2c-105">DESCRIPTION</span></span>
<span data-ttu-id="8ed2c-106">Mit dem Cmdlet **New-AzActionGroup** wird ein Aktionsgruppen-Referenzobjekt im Arbeitsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="8ed2c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ed2c-107">EXAMPLES</span></span>

### <span data-ttu-id="8ed2c-108">Beispiel 1: Erstellen eines Aktionsgruppen-Referenzobjekts im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="8ed2c-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="8ed2c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ed2c-109">PARAMETERS</span></span>

### <span data-ttu-id="8ed2c-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="8ed2c-110">-ActionGroupId</span></span>
<span data-ttu-id="8ed2c-111">Die ID/Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="8ed2c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed2c-112">-DefaultProfile</span></span>
<span data-ttu-id="8ed2c-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8ed2c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ed2c-114">-Webhookproperty</span><span class="sxs-lookup"><span data-stu-id="8ed2c-114">-WebhookProperty</span></span>
<span data-ttu-id="8ed2c-115">Die webhook-Eigenschaften der Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="8ed2c-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed2c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed2c-116">CommonParameters</span></span>
<span data-ttu-id="8ed2c-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed2c-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ed2c-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed2c-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ed2c-119">INPUTS</span></span>

### <span data-ttu-id="8ed2c-120">System. String</span><span class="sxs-lookup"><span data-stu-id="8ed2c-120">System.String</span></span>

### <span data-ttu-id="8ed2c-121">System. Collections. Generic. Dictionary ' 2 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. private. CoreLib, Version = 4.0.0.0, Kultur = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ed2c-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8ed2c-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ed2c-122">OUTPUTS</span></span>

### <span data-ttu-id="8ed2c-123">Microsoft. Azure. Management. Monitor. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="8ed2c-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="8ed2c-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ed2c-124">NOTES</span></span>

## <span data-ttu-id="8ed2c-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ed2c-125">RELATED LINKS</span></span>

[<span data-ttu-id="8ed2c-126">Satz-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8ed2c-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="8ed2c-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8ed2c-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="8ed2c-128">Deaktivieren-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8ed2c-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="8ed2c-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8ed2c-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="8ed2c-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8ed2c-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="8ed2c-131">Neu – AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="8ed2c-131">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

