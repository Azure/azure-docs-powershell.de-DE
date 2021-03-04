---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/resolve-azerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Resolve-AzError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Resolve-AzError.md
ms.openlocfilehash: e57eaed9865eacc6d783e6895bd3995c1b6a37ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920883"
---
# <span data-ttu-id="190c2-101">Resolve-AzError</span><span class="sxs-lookup"><span data-stu-id="190c2-101">Resolve-AzError</span></span>

## <span data-ttu-id="190c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="190c2-102">SYNOPSIS</span></span>
<span data-ttu-id="190c2-103">Zeigen Sie detaillierte Informationen zu PowerShell-Fehlern mit erweiterten Details für Azure PowerShell-Fehler an.</span><span class="sxs-lookup"><span data-stu-id="190c2-103">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

## <span data-ttu-id="190c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="190c2-104">SYNTAX</span></span>

### <span data-ttu-id="190c2-105">AnyErrorParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="190c2-105">AnyErrorParameterSet (Default)</span></span>
```
Resolve-AzError [[-Error] <ErrorRecord[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="190c2-106">LastErrorParameterSet</span><span class="sxs-lookup"><span data-stu-id="190c2-106">LastErrorParameterSet</span></span>
```
Resolve-AzError [-Last] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="190c2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="190c2-107">DESCRIPTION</span></span>
<span data-ttu-id="190c2-108">Löst und zeigt detaillierte Informationen zu Fehlern in der aktuellen PowerShell-Sitzung an, einschließlich der Stelle, an der der Fehler in Skript, Stapelverfolgung und allen inneren und aggregierten Ausnahmen aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="190c2-108">Resolves and displays detailed information about errors in the current PowerShell session, including where the error occurred in script, stack trace, and all inner and aggregate exceptions.</span></span> <span data-ttu-id="190c2-109">Bei Azure PowerShell-Fehlern werden zusätzliche Details zum Debuggen von Dienstproblemen bereitgestellt, einschließlich vollständiger Details zur Anforderung und Serverantwort, die den Fehler verursacht haben.</span><span class="sxs-lookup"><span data-stu-id="190c2-109">For Azure PowerShell errors provides additional detail in debugging service issues, including complete detail about the request and server response that caused the error.</span></span>

## <span data-ttu-id="190c2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="190c2-110">EXAMPLES</span></span>

### <span data-ttu-id="190c2-111">Beispiel 1: Beheben des letzten Fehlers</span><span class="sxs-lookup"><span data-stu-id="190c2-111">Example 1: Resolve the Last Error</span></span>
```
PS C:\> Resolve-AzError -Last

   HistoryId: 3


Message        : Run Connect-AzAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in AzureRmCmdlet.cs:line 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() inAzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzSubscription}
Line           : Get-AzSubscription
Position       : At line:1 char:1
                 + Get-AzSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 3
```

<span data-ttu-id="190c2-112">Hier erhalten Sie Details zum letzten Fehler.</span><span class="sxs-lookup"><span data-stu-id="190c2-112">Get details of the last error.</span></span>

### <span data-ttu-id="190c2-113">Beispiel 2: Beheben aller Fehler in der Sitzung</span><span class="sxs-lookup"><span data-stu-id="190c2-113">Example 2: Resolve all Errors in the Session</span></span>
```
PS C:\> Resolve-AzError


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzStorageAccount}
Line           : Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
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


Message        : Run Connect-AzAccount to login.
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
InvocationInfo : {Get-AzSubscription}
Line           : Get-AzSubscription
Position       : At line:1 char:1
                 + Get-AzSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 5
```

<span data-ttu-id="190c2-114">Hier erhalten Sie Details zu allen Fehlern, die in der aktuellen Sitzung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="190c2-114">Get details of all errors that have occurred in the current session.</span></span>

### <span data-ttu-id="190c2-115">Beispiel 3: Beheben eines bestimmten Fehlers</span><span class="sxs-lookup"><span data-stu-id="190c2-115">Example 3: Resolve a Specific Error</span></span>
```
PS C:\> Resolve-AzError $Error[0]


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzStorageAccount}
Line           : Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
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

<span data-ttu-id="190c2-116">Hier erhalten Sie Details zum angegebenen Fehler.</span><span class="sxs-lookup"><span data-stu-id="190c2-116">Get details of the specified error.</span></span>

## <span data-ttu-id="190c2-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="190c2-117">PARAMETERS</span></span>

### <span data-ttu-id="190c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="190c2-118">-DefaultProfile</span></span>
<span data-ttu-id="190c2-119">Die Anmeldeinformationen, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="190c2-119">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="190c2-120">-Fehler</span><span class="sxs-lookup"><span data-stu-id="190c2-120">-Error</span></span>
<span data-ttu-id="190c2-121">Mindestens ein Fehlerdatensätze, der aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="190c2-121">One or more error records to resolve.</span></span>  <span data-ttu-id="190c2-122">Wenn keine Parameter angegeben werden, werden alle Fehler in der Sitzung behoben.</span><span class="sxs-lookup"><span data-stu-id="190c2-122">If no parameters are specified, all errors in the session are resolved.</span></span>

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

### <span data-ttu-id="190c2-123">-Last</span><span class="sxs-lookup"><span data-stu-id="190c2-123">-Last</span></span>
<span data-ttu-id="190c2-124">Beheben Sie nur den letzten Fehler, der in der Sitzung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="190c2-124">Resolve only the last error that occurred in the session.</span></span>

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

### <span data-ttu-id="190c2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="190c2-125">CommonParameters</span></span>
<span data-ttu-id="190c2-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="190c2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="190c2-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="190c2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="190c2-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="190c2-128">INPUTS</span></span>

### <span data-ttu-id="190c2-129">System.Management.Automation.ErrorRecord[]</span><span class="sxs-lookup"><span data-stu-id="190c2-129">System.Management.Automation.ErrorRecord[]</span></span>

## <span data-ttu-id="190c2-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="190c2-130">OUTPUTS</span></span>

### <span data-ttu-id="190c2-131">Microsoft.Azure.Commands.Profile.Errors.AzureErrorRecord</span><span class="sxs-lookup"><span data-stu-id="190c2-131">Microsoft.Azure.Commands.Profile.Errors.AzureErrorRecord</span></span>

### <span data-ttu-id="190c2-132">Microsoft.Azure.Commands.Profile.Errors.AzureExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="190c2-132">Microsoft.Azure.Commands.Profile.Errors.AzureExceptionRecord</span></span>

### <span data-ttu-id="190c2-133">Microsoft.Azure.Commands.Profile.Errors.AzureRestExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="190c2-133">Microsoft.Azure.Commands.Profile.Errors.AzureRestExceptionRecord</span></span>

## <span data-ttu-id="190c2-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="190c2-134">NOTES</span></span>

## <span data-ttu-id="190c2-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="190c2-135">RELATED LINKS</span></span>
