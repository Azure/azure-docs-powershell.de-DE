---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: cb332c1aed8f828f893417561302ddcf36ba0cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497962"
---
# <span data-ttu-id="eb32c-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="eb32c-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="eb32c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb32c-102">SYNOPSIS</span></span>
<span data-ttu-id="eb32c-103">Erstellt eine Automatisierungs Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="eb32c-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb32c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb32c-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb32c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb32c-105">DESCRIPTION</span></span>
<span data-ttu-id="eb32c-106">Das Cmdlet **New-AzureRmAutomationCredential** erstellt eine Anmeldeinformationen als **PSCredential** -Objekt in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="eb32c-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="eb32c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb32c-107">EXAMPLES</span></span>

### <span data-ttu-id="eb32c-108">Beispiel 1: Erstellen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="eb32c-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="eb32c-109">Der erste Befehl weist der $User-Variablen einen Benutzernamen zu.</span><span class="sxs-lookup"><span data-stu-id="eb32c-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="eb32c-110">Mit dem zweiten Befehl wird ein nur-Text-Kennwort mithilfe des ConvertTo-SecureString-Cmdlets in eine sichere Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="eb32c-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="eb32c-111">Der Befehl speichert das Objekt in der $Password Variablen.</span><span class="sxs-lookup"><span data-stu-id="eb32c-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="eb32c-112">Der dritte Befehl erstellt eine Anmeldeinformationen basierend auf $User und $Password und speichert Sie dann in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="eb32c-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="eb32c-113">Der endgültige Befehl erstellt eine Automatisierungs Anmeldeinformationen mit dem Namen ContosoCredential, die $Credential verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb32c-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="eb32c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb32c-114">PARAMETERS</span></span>

### <span data-ttu-id="eb32c-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eb32c-115">-AutomationAccountName</span></span>
<span data-ttu-id="eb32c-116">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet die Anmeldeinformationen speichert.</span><span class="sxs-lookup"><span data-stu-id="eb32c-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="eb32c-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb32c-117">-Description</span></span>
<span data-ttu-id="eb32c-118">Gibt eine Beschreibung für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="eb32c-118">Specifies a description for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb32c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="eb32c-119">-Name</span></span>
<span data-ttu-id="eb32c-120">Gibt einen Namen für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="eb32c-120">Specifies a name for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb32c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb32c-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb32c-122">Gibt eine Beschreibung für die Ressourcengruppe an, für die dieses Cmdlet eine Anmeldeinformationen erstellt.</span><span class="sxs-lookup"><span data-stu-id="eb32c-122">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb32c-123">-Wert</span><span class="sxs-lookup"><span data-stu-id="eb32c-123">-Value</span></span>
<span data-ttu-id="eb32c-124">Gibt die Anmeldeinformationen als **PSCredential** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="eb32c-124">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb32c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb32c-125">-DefaultProfile</span></span>
<span data-ttu-id="eb32c-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb32c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb32c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb32c-127">CommonParameters</span></span>
<span data-ttu-id="eb32c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb32c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb32c-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb32c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb32c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb32c-130">INPUTS</span></span>

## <span data-ttu-id="eb32c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb32c-131">OUTPUTS</span></span>

### <span data-ttu-id="eb32c-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="eb32c-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="eb32c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb32c-133">NOTES</span></span>

## <span data-ttu-id="eb32c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb32c-134">RELATED LINKS</span></span>

[<span data-ttu-id="eb32c-135">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="eb32c-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="eb32c-136">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="eb32c-136">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="eb32c-137">Satz-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="eb32c-137">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


