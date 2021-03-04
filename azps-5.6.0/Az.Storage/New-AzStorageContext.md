---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: 4e4a86d5054a5554cb473c60550d32adffae5e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944519"
---
# <span data-ttu-id="611e8-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="611e8-101">New-AzStorageContext</span></span>

## <span data-ttu-id="611e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="611e8-102">SYNOPSIS</span></span>
<span data-ttu-id="611e8-103">Erstellt einen Azure Storage-Kontext.</span><span class="sxs-lookup"><span data-stu-id="611e8-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="611e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="611e8-104">SYNTAX</span></span>

### <span data-ttu-id="611e8-105">OAuthAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="611e8-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="611e8-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="611e8-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="611e8-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="611e8-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="611e8-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="611e8-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="611e8-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="611e8-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="611e8-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="611e8-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="611e8-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="611e8-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="611e8-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="611e8-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="611e8-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="611e8-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="611e8-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="611e8-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="611e8-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="611e8-115">DESCRIPTION</span></span>
<span data-ttu-id="611e8-116">Das **Cmdlet New-AzStorageContext** erstellt einen Azure Storage-Kontext.</span><span class="sxs-lookup"><span data-stu-id="611e8-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="611e8-117">Die Standardauthentifizierung eines Speicherkontexts ist OAuth (Azure AD), sofern nur der Name des Speicherkontos eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="611e8-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="611e8-118">Details zur Authentifizierung des Speicherdiensts finden Sie in https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services .</span><span class="sxs-lookup"><span data-stu-id="611e8-118">See details of authentication of the Storage Service in https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="611e8-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="611e8-119">EXAMPLES</span></span>

### <span data-ttu-id="611e8-120">Beispiel 1: Erstellen eines Kontexts durch Angeben eines Speicherkontonamens und -schlüssels</span><span class="sxs-lookup"><span data-stu-id="611e8-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="611e8-121">Mit diesem Befehl wird ein Kontext für das Konto namens ContosoGeneral erstellt, das den angegebenen Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="611e8-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="611e8-122">Beispiel 2: Erstellen eines Kontexts durch Angeben einer Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="611e8-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="611e8-123">Mit diesem Befehl wird ein Kontext basierend auf der angegebenen Verbindungszeichenfolge für das Konto ContosoGeneral erstellt.</span><span class="sxs-lookup"><span data-stu-id="611e8-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="611e8-124">Beispiel 3: Erstellen eines Kontexts für ein anonymes Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="611e8-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="611e8-125">Mit diesem Befehl wird ein Kontext für die anonyme Verwendung für das Konto namens ContosoGeneral erstellt.</span><span class="sxs-lookup"><span data-stu-id="611e8-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="611e8-126">Der Befehl gibt HTTP als Verbindungsprotokoll an.</span><span class="sxs-lookup"><span data-stu-id="611e8-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="611e8-127">Beispiel 4: Erstellen eines Kontexts mithilfe des lokalen Entwicklungsspeicherkontos</span><span class="sxs-lookup"><span data-stu-id="611e8-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="611e8-128">Mit diesem Befehl wird mithilfe des lokalen Entwicklungsspeicherkontos ein Kontext erstellt.</span><span class="sxs-lookup"><span data-stu-id="611e8-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="611e8-129">Der Befehl gibt den Parameter *Local* an.</span><span class="sxs-lookup"><span data-stu-id="611e8-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="611e8-130">Beispiel 5: Container für das lokale Entwicklerspeicherkonto</span><span class="sxs-lookup"><span data-stu-id="611e8-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="611e8-131">Dieser Befehl erstellt mithilfe des lokalen Entwicklungsspeicherkontos einen Kontext und übergibt dann den neuen Kontext mithilfe des Pipelineoperators an das **Get-AzStorageContainer-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="611e8-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="611e8-132">Der Befehl ruft den Azure Storage-Container für das lokale Entwicklerspeicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="611e8-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="611e8-133">Beispiel 6: Mehrere Container erhalten</span><span class="sxs-lookup"><span data-stu-id="611e8-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="611e8-134">Der erste Befehl erstellt einen Kontext mithilfe des lokalen Entwicklungsspeicherkontos und speichert diesen Kontext dann in der $Context 01.</span><span class="sxs-lookup"><span data-stu-id="611e8-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="611e8-135">Der zweite Befehl erstellt einen Kontext für das Konto namens ContosoGeneral, das den angegebenen Schlüssel verwendet, und speichert diesen Kontext dann in der $Context 02-Variable.</span><span class="sxs-lookup"><span data-stu-id="611e8-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="611e8-136">Der letzte Befehl ruft die Container für die Kontexte ab, die in $Context 01 und $Context 02 gespeichert sind, indem **Get-AzStorageContainer verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="611e8-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="611e8-137">Beispiel 7: Erstellen eines Kontexts mit einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="611e8-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="611e8-138">Mit diesem Befehl wird ein Azure Storage-Kontext erstellt, der den angegebenen Speicherendpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="611e8-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="611e8-139">Der Befehl erstellt den Kontext für das Konto namens ContosoGeneral, das den angegebenen Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="611e8-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="611e8-140">Beispiel 8: Erstellen eines Kontexts mit einer angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="611e8-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="611e8-141">Mit diesem Befehl wird ein Azure-Speicherkontext mit der angegebenen Azure-Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="611e8-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="611e8-142">Der Befehl erstellt den Kontext für das Konto namens ContosoGeneral, das den angegebenen Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="611e8-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="611e8-143">Beispiel 9: Erstellen eines Kontexts mithilfe eines SAS-Tokens</span><span class="sxs-lookup"><span data-stu-id="611e8-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="611e8-144">Der erste Befehl generiert ein SAS-Token mithilfe des **Cmdlets New-AzStorageContainerSASToken** für den Container namens ContosoMain und speichert dieses Token dann in der variablen $SasToken.</span><span class="sxs-lookup"><span data-stu-id="611e8-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="611e8-145">Dieses Token ist zum Lesen, Hinzufügen, Aktualisieren und Löschen von Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="611e8-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="611e8-146">Der zweite Befehl erstellt einen Kontext für das Konto namens ContosoGeneral, das das in $SasToken gespeicherte SAS-Token verwendet und diesen Kontext dann in der $Context speichert.</span><span class="sxs-lookup"><span data-stu-id="611e8-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="611e8-147">Der letzte Befehl listet alle blobs auf, die dem Container "ContosoMain" zugeordnet sind, indem der kontextbezogene Kontext verwendet wird, der in $Context.</span><span class="sxs-lookup"><span data-stu-id="611e8-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="611e8-148">Beispiel 10: Erstellen eines Kontexts mithilfe der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="611e8-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="611e8-149">Mit diesem Befehl wird mithilfe der OAuth (Azure AD)-Authentifizierung ein Kontext erstellt.</span><span class="sxs-lookup"><span data-stu-id="611e8-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="611e8-150">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="611e8-150">PARAMETERS</span></span>

### <span data-ttu-id="611e8-151">-Anonym</span><span class="sxs-lookup"><span data-stu-id="611e8-151">-Anonymous</span></span>
<span data-ttu-id="611e8-152">Gibt an, dass mit diesem Cmdlet ein Azure Storage-Kontext für die anonyme Anmeldung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="611e8-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611e8-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="611e8-153">-ConnectionString</span></span>
<span data-ttu-id="611e8-154">Gibt eine Verbindungszeichenfolge für den Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="611e8-154">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611e8-155">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="611e8-155">-Endpoint</span></span>
<span data-ttu-id="611e8-156">Gibt den Endpunkt für den Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="611e8-156">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611e8-157">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="611e8-157">-Environment</span></span>
<span data-ttu-id="611e8-158">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="611e8-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="611e8-159">Die zulässigen Werte für diesen Parameter sind: AzureCloud und AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="611e8-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="611e8-160">Weitere Informationen finden Sie unter `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="611e8-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="611e8-161">-Local</span><span class="sxs-lookup"><span data-stu-id="611e8-161">-Local</span></span>
<span data-ttu-id="611e8-162">Gibt an, dass dieses Cmdlet mithilfe des lokalen Entwicklungsspeicherkontos einen Kontext erstellt.</span><span class="sxs-lookup"><span data-stu-id="611e8-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611e8-163">-Protocol</span><span class="sxs-lookup"><span data-stu-id="611e8-163">-Protocol</span></span>
<span data-ttu-id="611e8-164">Transfer Protocol (https/http).</span><span class="sxs-lookup"><span data-stu-id="611e8-164">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611e8-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="611e8-165">-SasToken</span></span>
<span data-ttu-id="611e8-166">Gibt ein SAS-Token (Shared Access Signature) für den Kontext an.</span><span class="sxs-lookup"><span data-stu-id="611e8-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611e8-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="611e8-167">-StorageAccountKey</span></span>
<span data-ttu-id="611e8-168">Gibt einen Azure Storage-Kontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="611e8-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="611e8-169">Dieses Cmdlet erstellt einen Kontext für den Schlüssel, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="611e8-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611e8-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="611e8-170">-StorageAccountName</span></span>
<span data-ttu-id="611e8-171">Gibt einen Azure Storage-Kontonamen an.</span><span class="sxs-lookup"><span data-stu-id="611e8-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="611e8-172">Dieses Cmdlet erstellt einen Kontext für das Konto, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="611e8-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611e8-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="611e8-173">-UseConnectedAccount</span></span>
<span data-ttu-id="611e8-174">Gibt an, dass mit diesem Cmdlet ein Azure Storage-Kontext mit der OAuth (Azure AD)-Authentifizierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="611e8-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="611e8-175">Das Cmdlet verwendet standardmäßig die OAuth-Authentifizierung, wenn keine andere Authentifizierung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="611e8-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611e8-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="611e8-176">CommonParameters</span></span>
<span data-ttu-id="611e8-177">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="611e8-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="611e8-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="611e8-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="611e8-179">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="611e8-179">INPUTS</span></span>

### <span data-ttu-id="611e8-180">System.String</span><span class="sxs-lookup"><span data-stu-id="611e8-180">System.String</span></span>

## <span data-ttu-id="611e8-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="611e8-181">OUTPUTS</span></span>

### <span data-ttu-id="611e8-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="611e8-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="611e8-183">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="611e8-183">NOTES</span></span>

## <span data-ttu-id="611e8-184">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="611e8-184">RELATED LINKS</span></span>

[<span data-ttu-id="611e8-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="611e8-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="611e8-186">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="611e8-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


