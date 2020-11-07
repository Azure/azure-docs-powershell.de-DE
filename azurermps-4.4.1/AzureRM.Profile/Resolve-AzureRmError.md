---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Resolve-AzureRmError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Resolve-AzureRmError.md
ms.openlocfilehash: 13bcf2e0b7e194801c45f725f7376b804c4ca045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665005"
---
# <span data-ttu-id="9ce02-101">Resolve-AzureRmError</span><span class="sxs-lookup"><span data-stu-id="9ce02-101">Resolve-AzureRmError</span></span>

## <span data-ttu-id="9ce02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ce02-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce02-103">Zeigen Sie detaillierte Informationen zu PowerShell-Fehlern mit erweiterten Details für Azure PowerShell-Fehler an.</span><span class="sxs-lookup"><span data-stu-id="9ce02-103">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ce02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ce02-104">SYNTAX</span></span>

### <span data-ttu-id="9ce02-105">AnyErrorParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ce02-105">AnyErrorParameterSet (Default)</span></span>
```
Resolve-AzureRmError [[-Error] <ErrorRecord[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ce02-106">LastErrorParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ce02-106">LastErrorParameterSet</span></span>
```
Resolve-AzureRmError [-Last] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ce02-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ce02-107">DESCRIPTION</span></span>
<span data-ttu-id="9ce02-108">Behebt und zeigt detaillierte Informationen zu Fehlern in der aktuellen PowerShell-Sitzung an, einschließlich der Fehler im Skript, in der Stapelüberwachung sowie in allen inneren und Aggregat Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="9ce02-108">Resolves and displays detailed information about errors in the current PowerShell session, including where the error occurred in script, stack trace, and all inner and aggregate exceptions.</span></span> <span data-ttu-id="9ce02-109">Für Azure PowerShell-Fehler bietet zusätzliche Informationen zum Debuggen von Dienstproblemen, einschließlich vollständiger Details zur Anforderung und Serverantwort, die den Fehler verursacht haben.</span><span class="sxs-lookup"><span data-stu-id="9ce02-109">For Azure PowerShell errors provides additional detail in debugging service issues, including complete detail about the request and server response that caused the error.</span></span>

## <span data-ttu-id="9ce02-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ce02-110">EXAMPLES</span></span>

### <span data-ttu-id="9ce02-111">Beispiel 1: Beheben des letzten Fehlers</span><span class="sxs-lookup"><span data-stu-id="9ce02-111">Example 1: Resolve the Last Error</span></span>
```
PS C:\> Resolve-AzureRmError -Last

   HistoryId: 3


Message        : Run Login-AzureRmAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in AzureRmCmdlet.cs:line 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() inAzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzureRmSubscription}
Line           : Get-AzureRmSubscription
Position       : At line:1 char:1
                 + Get-AzureRmSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 3
```

<span data-ttu-id="9ce02-112">Abrufen von Details zum letzten Fehler</span><span class="sxs-lookup"><span data-stu-id="9ce02-112">Get details of the last error.</span></span>

### <span data-ttu-id="9ce02-113">Beispiel 2: Beheben aller Fehler in der Sitzung</span><span class="sxs-lookup"><span data-stu-id="9ce02-113">Example 2: Resolve all Errors in the Session</span></span>
```
PS C:\> Resolve-AzureRmError


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzureRmStorageAccount}
Line           : Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8


   HistoryId: 5


Message        : Run Login-AzureRmAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in C:\zd\azur
                 e-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in
                 C:\zd\azure-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:lin
                 e 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in C:\zd\azure-p
                 owershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in C:\zd\azure-
                 powershell\src\ResourceManager\Profile\Commands.Profile\Subscription\GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzureRmSubscription}
Line           : Get-AzureRmSubscription
Position       : At line:1 char:1
                 + Get-AzureRmSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 5
```

<span data-ttu-id="9ce02-114">Abrufen von Details zu allen Fehlern, die in der aktuellen Sitzung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="9ce02-114">Get details of all errors that have occurred in the current session.</span></span>

### <span data-ttu-id="9ce02-115">Beispiel 3: Beheben eines bestimmten Fehlers</span><span class="sxs-lookup"><span data-stu-id="9ce02-115">Example 3: Resolve a Specific Error</span></span>
```
PS C:\> Resolve-AzureRmError $Error[0]


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzureRmStorageAccount}
Line           : Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8
```

<span data-ttu-id="9ce02-116">Abrufen von Details zum angegebenen Fehler</span><span class="sxs-lookup"><span data-stu-id="9ce02-116">Get details of the specified error.</span></span>

## <span data-ttu-id="9ce02-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ce02-117">PARAMETERS</span></span>

### <span data-ttu-id="9ce02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ce02-118">-DefaultProfile</span></span>
<span data-ttu-id="9ce02-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="9ce02-119">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce02-120">-Fehler</span><span class="sxs-lookup"><span data-stu-id="9ce02-120">-Error</span></span>
<span data-ttu-id="9ce02-121">Eine oder mehrere Fehlereinträge, die aufgelöst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9ce02-121">One or more error records to resolve.</span></span>  <span data-ttu-id="9ce02-122">Wenn keine Parameter angegeben werden, werden alle Fehler in der Sitzung aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="9ce02-122">If no parameters are specified, all errors in the session are resolved.</span></span>

```yaml
Type: System.Management.Automation.ErrorRecord[]
Parameter Sets: AnyErrorParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce02-123">-Letzte</span><span class="sxs-lookup"><span data-stu-id="9ce02-123">-Last</span></span>
<span data-ttu-id="9ce02-124">Beheben Sie nur den letzten Fehler, der in der Sitzung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9ce02-124">Resolve only the last error that occurred in the session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LastErrorParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce02-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce02-125">CommonParameters</span></span>
<span data-ttu-id="9ce02-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ce02-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce02-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ce02-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce02-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ce02-128">INPUTS</span></span>

### <span data-ttu-id="9ce02-129">System. Management. Automation. ErrorRecord []</span><span class="sxs-lookup"><span data-stu-id="9ce02-129">System.Management.Automation.ErrorRecord[]</span></span>

## <span data-ttu-id="9ce02-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ce02-130">OUTPUTS</span></span>

### <span data-ttu-id="9ce02-131">Microsoft. Azure. Commands. profile. Errors. AzureErrorRecord</span><span class="sxs-lookup"><span data-stu-id="9ce02-131">Microsoft.Azure.Commands.Profile.Errors.AzureErrorRecord</span></span>
<span data-ttu-id="9ce02-132">Informationen zu einem PowerShell-Fehler, bei dem es sich nicht um einen Exception handelt.</span><span class="sxs-lookup"><span data-stu-id="9ce02-132">Information about a powershell error that does not involve an excpetion.</span></span>

### <span data-ttu-id="9ce02-133">Microsoft. Azure. Commands. profile. Errors. AzureExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="9ce02-133">Microsoft.Azure.Commands.Profile.Errors.AzureExceptionRecord</span></span>
<span data-ttu-id="9ce02-134">Informationen zu einem Fehler einschließlich detaillierter Informationen zu der Ausnahme, die den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="9ce02-134">Information about an error including detailed information on the exception that raised the error.</span></span>

### <span data-ttu-id="9ce02-135">Microsoft. Azure. Commands. profile. Errors. AzureRestExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="9ce02-135">Microsoft.Azure.Commands.Profile.Errors.AzureRestExceptionRecord</span></span>
<span data-ttu-id="9ce02-136">Informationen zu Fehlern in der Cleint/Server-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="9ce02-136">Information about errors in cleint/server communications.</span></span>  <span data-ttu-id="9ce02-137">Dies enthält häufig wichtige Informationen zum Fehler vom Server.</span><span class="sxs-lookup"><span data-stu-id="9ce02-137">This will often contain important information about the error from the server.</span></span>

## <span data-ttu-id="9ce02-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ce02-138">NOTES</span></span>

## <span data-ttu-id="9ce02-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ce02-139">RELATED LINKS</span></span>

