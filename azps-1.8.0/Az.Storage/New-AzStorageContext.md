---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: 4c506906be76582a77d4a51ae7f103968060b451
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658820"
---
# <span data-ttu-id="7e984-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e984-101">New-AzStorageContext</span></span>

## <span data-ttu-id="7e984-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e984-102">SYNOPSIS</span></span>
<span data-ttu-id="7e984-103">Erstellt einen Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="7e984-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="7e984-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e984-104">SYNTAX</span></span>

### <span data-ttu-id="7e984-105">OAuthAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e984-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="7e984-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="7e984-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="7e984-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e984-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="7e984-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="7e984-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e984-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e984-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="7e984-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="7e984-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="7e984-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e984-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="7e984-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e984-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="7e984-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="7e984-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="7e984-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="7e984-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="7e984-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e984-115">DESCRIPTION</span></span>
<span data-ttu-id="7e984-116">Das Cmdlet **New-AzStorageContext** erstellt einen Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="7e984-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="7e984-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e984-117">EXAMPLES</span></span>

### <span data-ttu-id="7e984-118">Beispiel 1: Erstellen eines Kontexts durch Angeben eines Speicherkonto namens und-Schlüssels</span><span class="sxs-lookup"><span data-stu-id="7e984-118">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="7e984-119">Dieser Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e984-119">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="7e984-120">Beispiel 2: Erstellen eines Kontexts durch Angeben einer Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7e984-120">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="7e984-121">Dieser Befehl erstellt einen Kontext basierend auf der angegebenen Verbindungszeichenfolge für das Konto ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="7e984-121">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="7e984-122">Beispiel 3: Erstellen eines Kontexts für ein anonymes Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="7e984-122">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="7e984-123">Dieser Befehl erstellt einen Kontext für die anonyme Verwendung für das Konto mit dem Namen ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="7e984-123">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="7e984-124">Der Befehl gibt HTTP als Verbindungsprotokoll an.</span><span class="sxs-lookup"><span data-stu-id="7e984-124">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="7e984-125">Beispiel 4: Erstellen eines Kontexts mithilfe des lokalen entwicklungsspeicher Kontos</span><span class="sxs-lookup"><span data-stu-id="7e984-125">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="7e984-126">Dieser Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos.</span><span class="sxs-lookup"><span data-stu-id="7e984-126">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="7e984-127">Der Befehl gibt den *lokalen* Parameter an.</span><span class="sxs-lookup"><span data-stu-id="7e984-127">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="7e984-128">Beispiel 5: Abrufen des Containers für das lokale Entwickler Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="7e984-128">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="7e984-129">Dieser Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos und übergibt dann den neuen Kontext mithilfe des Pipelineoperators an das Cmdlet " **Get-AzStorageContainer** ".</span><span class="sxs-lookup"><span data-stu-id="7e984-129">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7e984-130">Der Befehl ruft den Azure-Speichercontainer für das lokale Entwickler Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="7e984-130">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="7e984-131">Beispiel 6: Abrufen mehrerer Container</span><span class="sxs-lookup"><span data-stu-id="7e984-131">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="7e984-132">Der erste Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos und speichert diesen Kontext dann in der $Context 01-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7e984-132">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="7e984-133">Der zweite Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird, und speichert diesen Kontext dann in der Variablen $Context 02.</span><span class="sxs-lookup"><span data-stu-id="7e984-133">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="7e984-134">Der endgültige Befehl ruft die Container für die in $context 01 und $Context 02 gespeicherten Kontexte ab, indem **Sie Get-AzStorageContainer** verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e984-134">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="7e984-135">Beispiel 7: Erstellen eines Kontexts mit einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="7e984-135">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="7e984-136">Dieser Befehl erstellt einen Azure-Speicherkontext mit dem angegebenen Speicher Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="7e984-136">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="7e984-137">Der Befehl erstellt den Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e984-137">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="7e984-138">Beispiel 8: Erstellen eines Kontexts mit einer angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="7e984-138">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="7e984-139">Mit diesem Befehl wird ein Azure-Speicherkontext mit der angegebenen Azure-Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e984-139">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="7e984-140">Der Befehl erstellt den Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e984-140">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="7e984-141">Beispiel 9: Erstellen eines Kontexts mithilfe eines SAS-Tokens</span><span class="sxs-lookup"><span data-stu-id="7e984-141">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="7e984-142">Der erste Befehl generiert ein SAS-Token mithilfe des Cmdlets **New-AzStorageContainerSASToken** für den Container mit dem Namen ContosoMain und speichert dieses Token dann in der $SasToken-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7e984-142">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="7e984-143">Dieses Token dient zum Lesen, hinzufügen, aktualisieren und Löschen von Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="7e984-143">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="7e984-144">Der zweite Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, das das in $SasToken gespeicherte SAS-Token verwendet, und speichert diesen Kontext dann in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="7e984-144">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="7e984-145">Der endgültige Befehl listet alle BLOBs auf, die dem Container mit dem Namen ContosoMain zugeordnet sind, indem Sie den in $context gespeicherten Kontext verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e984-145">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="7e984-146">Beispiel 10: Erstellen eines Kontexts mithilfe der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="7e984-146">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="7e984-147">Dieser Befehl erstellt einen Kontext mithilfe der OAuth-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7e984-147">This command creates a context by using the OAuth Authentication.</span></span>

## <span data-ttu-id="7e984-148">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e984-148">PARAMETERS</span></span>

### <span data-ttu-id="7e984-149">-Anonymous</span><span class="sxs-lookup"><span data-stu-id="7e984-149">-Anonymous</span></span>
<span data-ttu-id="7e984-150">Gibt an, dass mit diesem Cmdlet ein Azure-Speicherkontext für die anonyme Anmeldung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7e984-150">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="7e984-151">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="7e984-151">-ConnectionString</span></span>
<span data-ttu-id="7e984-152">Gibt eine Verbindungszeichenfolge für den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="7e984-152">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="7e984-153">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="7e984-153">-Endpoint</span></span>
<span data-ttu-id="7e984-154">Gibt den Endpunkt für den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="7e984-154">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="7e984-155">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="7e984-155">-Environment</span></span>
<span data-ttu-id="7e984-156">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="7e984-156">Specifies the Azure environment.</span></span>
<span data-ttu-id="7e984-157">Die zulässigen Werte für diesen Parameter sind: AzureCloud und AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="7e984-157">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="7e984-158">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="7e984-158">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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

### <span data-ttu-id="7e984-159">-Lokal</span><span class="sxs-lookup"><span data-stu-id="7e984-159">-Local</span></span>
<span data-ttu-id="7e984-160">Gibt an, dass dieses Cmdlet einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e984-160">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="7e984-161">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="7e984-161">-Protocol</span></span>
<span data-ttu-id="7e984-162">Übertragungsprotokoll (HTTPS/HTTP).</span><span class="sxs-lookup"><span data-stu-id="7e984-162">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="7e984-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="7e984-163">-SasToken</span></span>
<span data-ttu-id="7e984-164">Gibt ein SAS-Token (Shared Access Signature) für den Kontext an.</span><span class="sxs-lookup"><span data-stu-id="7e984-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="7e984-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7e984-165">-StorageAccountKey</span></span>
<span data-ttu-id="7e984-166">Gibt einen Azure-speicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="7e984-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="7e984-167">Dieses Cmdlet erstellt einen Kontext für den Schlüssel, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7e984-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="7e984-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7e984-168">-StorageAccountName</span></span>
<span data-ttu-id="7e984-169">Gibt den Namen eines Azure-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="7e984-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="7e984-170">Dieses Cmdlet erstellt einen Kontext für das Konto, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7e984-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="7e984-171">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="7e984-171">-UseConnectedAccount</span></span>
<span data-ttu-id="7e984-172">Gibt an, dass mit diesem Cmdlet ein Azure-Speicherkontext mit OAuth-Authentifizierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7e984-172">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="7e984-173">Das Cmdlet verwendet standardmäßig die OAuth-Authentifizierung, wenn andere anthentication nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7e984-173">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

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

### <span data-ttu-id="7e984-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e984-174">CommonParameters</span></span>
<span data-ttu-id="7e984-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e984-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e984-176">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e984-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e984-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e984-177">INPUTS</span></span>

### <span data-ttu-id="7e984-178">System. String</span><span class="sxs-lookup"><span data-stu-id="7e984-178">System.String</span></span>

## <span data-ttu-id="7e984-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e984-179">OUTPUTS</span></span>

### <span data-ttu-id="7e984-180">Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e984-180">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="7e984-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e984-181">NOTES</span></span>

## <span data-ttu-id="7e984-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e984-182">RELATED LINKS</span></span>

[<span data-ttu-id="7e984-183">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7e984-183">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="7e984-184">Neu – AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="7e984-184">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


