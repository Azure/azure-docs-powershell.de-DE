---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177374"
---
# <span data-ttu-id="114dc-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="114dc-101">New-AzStorageContext</span></span>

## <span data-ttu-id="114dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="114dc-102">SYNOPSIS</span></span>
<span data-ttu-id="114dc-103">Erstellt einen Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="114dc-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="114dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="114dc-104">SYNTAX</span></span>

### <span data-ttu-id="114dc-105">OAuthAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="114dc-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="114dc-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="114dc-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="114dc-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="114dc-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="114dc-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="114dc-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="114dc-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="114dc-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="114dc-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="114dc-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="114dc-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="114dc-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="114dc-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="114dc-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="114dc-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="114dc-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="114dc-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="114dc-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="114dc-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="114dc-115">DESCRIPTION</span></span>
<span data-ttu-id="114dc-116">Das Cmdlet **New-AzStorageContext** erstellt einen Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="114dc-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="114dc-117">Die Standardauthentifizierung eines Speicher Kontexts ist OAuth (Azure AD), wenn nur der Name des Eingabe speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="114dc-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="114dc-118">Details zur Authentifizierung des Speicher Diensts finden Sie unter https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .</span><span class="sxs-lookup"><span data-stu-id="114dc-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="114dc-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="114dc-119">EXAMPLES</span></span>

### <span data-ttu-id="114dc-120">Beispiel 1: Erstellen eines Kontexts durch Angeben eines Speicherkonto namens und-Schlüssels</span><span class="sxs-lookup"><span data-stu-id="114dc-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="114dc-121">Dieser Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="114dc-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="114dc-122">Beispiel 2: Erstellen eines Kontexts durch Angeben einer Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="114dc-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="114dc-123">Dieser Befehl erstellt einen Kontext basierend auf der angegebenen Verbindungszeichenfolge für das Konto ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="114dc-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="114dc-124">Beispiel 3: Erstellen eines Kontexts für ein anonymes Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="114dc-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="114dc-125">Dieser Befehl erstellt einen Kontext für die anonyme Verwendung für das Konto mit dem Namen ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="114dc-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="114dc-126">Der Befehl gibt HTTP als Verbindungsprotokoll an.</span><span class="sxs-lookup"><span data-stu-id="114dc-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="114dc-127">Beispiel 4: Erstellen eines Kontexts mithilfe des lokalen entwicklungsspeicher Kontos</span><span class="sxs-lookup"><span data-stu-id="114dc-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="114dc-128">Dieser Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos.</span><span class="sxs-lookup"><span data-stu-id="114dc-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="114dc-129">Der Befehl gibt den *lokalen* Parameter an.</span><span class="sxs-lookup"><span data-stu-id="114dc-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="114dc-130">Beispiel 5: Abrufen des Containers für das lokale Entwickler Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="114dc-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="114dc-131">Dieser Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos und übergibt dann den neuen Kontext mithilfe des Pipelineoperators an das Cmdlet " **Get-AzStorageContainer** ".</span><span class="sxs-lookup"><span data-stu-id="114dc-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="114dc-132">Der Befehl ruft den Azure-Speichercontainer für das lokale Entwickler Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="114dc-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="114dc-133">Beispiel 6: Abrufen mehrerer Container</span><span class="sxs-lookup"><span data-stu-id="114dc-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="114dc-134">Der erste Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos und speichert diesen Kontext dann in der $Context 01-Variablen.</span><span class="sxs-lookup"><span data-stu-id="114dc-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="114dc-135">Der zweite Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird, und speichert diesen Kontext dann in der Variablen $Context 02.</span><span class="sxs-lookup"><span data-stu-id="114dc-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="114dc-136">Der endgültige Befehl ruft die Container für die in $context 01 und $Context 02 gespeicherten Kontexte ab, indem **Sie Get-AzStorageContainer** verwenden.</span><span class="sxs-lookup"><span data-stu-id="114dc-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="114dc-137">Beispiel 7: Erstellen eines Kontexts mit einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="114dc-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="114dc-138">Dieser Befehl erstellt einen Azure-Speicherkontext mit dem angegebenen Speicher Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="114dc-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="114dc-139">Der Befehl erstellt den Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="114dc-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="114dc-140">Beispiel 8: Erstellen eines Kontexts mit einer angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="114dc-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="114dc-141">Mit diesem Befehl wird ein Azure-Speicherkontext mit der angegebenen Azure-Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="114dc-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="114dc-142">Der Befehl erstellt den Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="114dc-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="114dc-143">Beispiel 9: Erstellen eines Kontexts mithilfe eines SAS-Tokens</span><span class="sxs-lookup"><span data-stu-id="114dc-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="114dc-144">Der erste Befehl generiert ein SAS-Token mithilfe des Cmdlets **New-AzStorageContainerSASToken** für den Container mit dem Namen ContosoMain und speichert dieses Token dann in der $SasToken-Variablen.</span><span class="sxs-lookup"><span data-stu-id="114dc-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="114dc-145">Dieses Token dient zum Lesen, hinzufügen, aktualisieren und Löschen von Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="114dc-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="114dc-146">Der zweite Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, das das in $SasToken gespeicherte SAS-Token verwendet, und speichert diesen Kontext dann in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="114dc-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="114dc-147">Der endgültige Befehl listet alle BLOBs auf, die dem Container mit dem Namen ContosoMain zugeordnet sind, indem Sie den in $context gespeicherten Kontext verwenden.</span><span class="sxs-lookup"><span data-stu-id="114dc-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="114dc-148">Beispiel 10: Erstellen eines Kontexts mithilfe der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="114dc-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="114dc-149">Dieser Befehl erstellt einen Kontext mithilfe der OAuth (Azure AD)-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="114dc-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="114dc-150">Parameter</span><span class="sxs-lookup"><span data-stu-id="114dc-150">PARAMETERS</span></span>

### <span data-ttu-id="114dc-151">-Anonymous</span><span class="sxs-lookup"><span data-stu-id="114dc-151">-Anonymous</span></span>
<span data-ttu-id="114dc-152">Gibt an, dass mit diesem Cmdlet ein Azure-Speicherkontext für die anonyme Anmeldung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="114dc-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="114dc-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="114dc-153">-ConnectionString</span></span>
<span data-ttu-id="114dc-154">Gibt eine Verbindungszeichenfolge für den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="114dc-154">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="114dc-155">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="114dc-155">-Endpoint</span></span>
<span data-ttu-id="114dc-156">Gibt den Endpunkt für den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="114dc-156">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="114dc-157">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="114dc-157">-Environment</span></span>
<span data-ttu-id="114dc-158">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="114dc-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="114dc-159">Die zulässigen Werte für diesen Parameter sind: AzureCloud und AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="114dc-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="114dc-160">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="114dc-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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

### <span data-ttu-id="114dc-161">-Lokal</span><span class="sxs-lookup"><span data-stu-id="114dc-161">-Local</span></span>
<span data-ttu-id="114dc-162">Gibt an, dass dieses Cmdlet einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos erstellt.</span><span class="sxs-lookup"><span data-stu-id="114dc-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="114dc-163">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="114dc-163">-Protocol</span></span>
<span data-ttu-id="114dc-164">Übertragungsprotokoll (HTTPS/HTTP).</span><span class="sxs-lookup"><span data-stu-id="114dc-164">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="114dc-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="114dc-165">-SasToken</span></span>
<span data-ttu-id="114dc-166">Gibt ein SAS-Token (Shared Access Signature) für den Kontext an.</span><span class="sxs-lookup"><span data-stu-id="114dc-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="114dc-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="114dc-167">-StorageAccountKey</span></span>
<span data-ttu-id="114dc-168">Gibt einen Azure-speicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="114dc-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="114dc-169">Dieses Cmdlet erstellt einen Kontext für den Schlüssel, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="114dc-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="114dc-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="114dc-170">-StorageAccountName</span></span>
<span data-ttu-id="114dc-171">Gibt den Namen eines Azure-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="114dc-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="114dc-172">Dieses Cmdlet erstellt einen Kontext für das Konto, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="114dc-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="114dc-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="114dc-173">-UseConnectedAccount</span></span>
<span data-ttu-id="114dc-174">Gibt an, dass mit diesem Cmdlet ein Azure-Speicherkontext mit OAuth (Azure AD)-Authentifizierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="114dc-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="114dc-175">Das Cmdlet verwendet standardmäßig die OAuth-Authentifizierung, wenn keine andere Authentifizierung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="114dc-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

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

### <span data-ttu-id="114dc-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114dc-176">CommonParameters</span></span>
<span data-ttu-id="114dc-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="114dc-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114dc-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="114dc-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114dc-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="114dc-179">INPUTS</span></span>

### <span data-ttu-id="114dc-180">System. String</span><span class="sxs-lookup"><span data-stu-id="114dc-180">System.String</span></span>

## <span data-ttu-id="114dc-181">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="114dc-181">OUTPUTS</span></span>

### <span data-ttu-id="114dc-182">Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="114dc-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="114dc-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="114dc-183">NOTES</span></span>

## <span data-ttu-id="114dc-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="114dc-184">RELATED LINKS</span></span>

[<span data-ttu-id="114dc-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="114dc-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="114dc-186">Neu – AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="114dc-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


