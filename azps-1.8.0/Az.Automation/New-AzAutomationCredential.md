---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a4d28affaa44e96a713adea7935073bcdf9d93c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661780"
---
# <span data-ttu-id="9175e-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9175e-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="9175e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9175e-102">SYNOPSIS</span></span>
<span data-ttu-id="9175e-103">Erstellt eine Automatisierungs Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="9175e-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="9175e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9175e-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9175e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9175e-105">DESCRIPTION</span></span>
<span data-ttu-id="9175e-106">Das Cmdlet **New-AzAutomationCredential** erstellt eine Anmeldeinformationen als **PSCredential** -Objekt in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="9175e-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="9175e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9175e-107">EXAMPLES</span></span>

### <span data-ttu-id="9175e-108">Beispiel 1: Erstellen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="9175e-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9175e-109">Der erste Befehl weist der $User-Variablen einen Benutzernamen zu.</span><span class="sxs-lookup"><span data-stu-id="9175e-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="9175e-110">Mit dem zweiten Befehl wird ein nur-Text-Kennwort mithilfe des ConvertTo-SecureString-Cmdlets in eine sichere Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="9175e-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="9175e-111">Der Befehl speichert das Objekt in der $Password Variablen.</span><span class="sxs-lookup"><span data-stu-id="9175e-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="9175e-112">Der dritte Befehl erstellt eine Anmeldeinformationen basierend auf $User und $Password und speichert Sie dann in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="9175e-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="9175e-113">Der endgültige Befehl erstellt eine Automatisierungs Anmeldeinformationen mit dem Namen ContosoCredential, die $Credential verwendet.</span><span class="sxs-lookup"><span data-stu-id="9175e-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="9175e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9175e-114">PARAMETERS</span></span>

### <span data-ttu-id="9175e-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9175e-115">-AutomationAccountName</span></span>
<span data-ttu-id="9175e-116">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet die Anmeldeinformationen speichert.</span><span class="sxs-lookup"><span data-stu-id="9175e-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="9175e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9175e-117">-DefaultProfile</span></span>
<span data-ttu-id="9175e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9175e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9175e-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9175e-119">-Description</span></span>
<span data-ttu-id="9175e-120">Gibt eine Beschreibung für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="9175e-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="9175e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9175e-121">-Name</span></span>
<span data-ttu-id="9175e-122">Gibt einen Namen für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="9175e-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="9175e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9175e-123">-ResourceGroupName</span></span>
<span data-ttu-id="9175e-124">Gibt eine Beschreibung für die Ressourcengruppe an, für die dieses Cmdlet eine Anmeldeinformationen erstellt.</span><span class="sxs-lookup"><span data-stu-id="9175e-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="9175e-125">-Wert</span><span class="sxs-lookup"><span data-stu-id="9175e-125">-Value</span></span>
<span data-ttu-id="9175e-126">Gibt die Anmeldeinformationen als **PSCredential** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9175e-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="9175e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9175e-127">CommonParameters</span></span>
<span data-ttu-id="9175e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9175e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9175e-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9175e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9175e-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9175e-130">INPUTS</span></span>

### <span data-ttu-id="9175e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9175e-131">System.String</span></span>

### <span data-ttu-id="9175e-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="9175e-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="9175e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9175e-133">OUTPUTS</span></span>

### <span data-ttu-id="9175e-134">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="9175e-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="9175e-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="9175e-135">NOTES</span></span>

## <span data-ttu-id="9175e-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9175e-136">RELATED LINKS</span></span>

[<span data-ttu-id="9175e-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9175e-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="9175e-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9175e-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="9175e-139">Satz-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9175e-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


